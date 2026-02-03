---
title: Toxic Language
createdAt: Wed Nov 12 2025 19:00:24 GMT+0000 (Coordinated Universal Time)
updatedAt: Thu Nov 27 2025 17:22:01 GMT+0000 (Coordinated Universal Time)
---

The toxic language guardrail detects harmful content including hate speech, threats, insults, and other communication that could damage your community or brand. Unlike simple keyword filters, this guardrail uses AI to understand context, tone, and intent.

knmknknkjn

![]()

## When to Use This Guardrail

![]()



![](https://api.archbee.com/api/optimize/511c8QBH-VHiwWnyzIwUb/kbsTYnFlRheDZpcjZzzNr_image.png)

The key advantage over simple keyword filtering is that this guardrail understands nuance. Someone can be hostile without using profanity, and they can use strong language without being hostile. The guardrail analyzes intent and tone, not just word choice.

## Understanding Sensitivity Levels

The sensitivity setting controls how strict the guardrail is. Think of it as adjusting the threshold for what constitutes a violation. This is one of the most important configuration choices you'll make because it fundamentally changes what content passes or fails.

Low sensitivity flags only severe violations like explicit threats and extreme hate speech. When you set sensitivity to low, you're saying that you expect strong opinions and robust disagreement, and you only want to block content that crosses a clear line into threatening or hateful territory. For example, "I strongly disagree with this approach and think it's misguided" would pass at low sensitivity, as would "This is a terrible idea." Only content like "I will find you and hurt you" or explicit hate speech would fail.

Low sensitivity works well for public forums where debate is expected, professional feedback environments where directness is valued, and technical communities where people discuss contentious topics. The tradeoff is that some content that makes people uncomfortable might still pass through.

Medium sensitivity is the default setting and represents a balanced approach. At this level, the guardrail flags clear violations including insults and hostile language while still allowing professional disagreement and constructive criticism. A message like "I disagree with your reasoning" would pass, but "You're an idiot" or "People like you are the problem" would fail.

Medium sensitivity works well for most applications including customer service systems, business communications, collaborative tools, and social platforms. It strikes a balance between allowing meaningful discourse and maintaining a respectful environment.

High sensitivity creates the strictest environment by flagging any potentially toxic content including mild rudeness and dismissive language. At this level, even content like "Whatever, dude" or "That's pretty dumb" would fail. Only respectful, neutral content passes at high sensitivity.

High sensitivity is appropriate for children's applications where you need maximum protection, educational platforms where you want to model respectful communication, safe spaces and support communities where people need to feel secure, and compliance-critical contexts where any potential issue needs to be caught.

## Configuration Options

The toxic language guardrail accepts several configuration options that let you tune its behavior for your specific use case.

```typescript
// Available options:
// sensitivity: "low", "medium", or "high" (default: "medium")
// model: model identifier (default: Claude 3.5 Haiku)
// temperature: 0-1, lower values = more consistent (default: 0.1)
// maxTokens: response length limit (default: 200)

await abv.guardrails.toxicLanguage.validate(text, {
  sensitivity: "medium",
  model: "model-name",
  temperature: 0.1,
  maxTokens: 200,
});
```

```python
# Available options:
# sensitivity: "low", "medium", or "high" (default: "medium")
# model: model identifier (default: Claude 3.5 Haiku)
# temperature: 0-1, lower values = more consistent (default: 0.1)
# maxTokens: response length limit (default: 200)

abv.guardrails.toxic_language.validate(text, {
    "sensitivity": "medium",
    "model": "model-name",
    "temperature": 0.1,
    "maxTokens": 200
})
```

The sensitivity option is the most important and you'll use it frequently. The model, temperature, and maxTokens options are advanced settings that you typically won't need to change. The default model is optimized for guardrail tasks and provides the best balance of speed, accuracy, and cost. The default temperature of 0.1 ensures consistent results. The default maxTokens of 200 is sufficient for the explanation field.

## Real-World Examples

Let's look at concrete examples of how different sensitivity levels handle various types of content. Understanding these patterns will help you choose the right sensitivity for your application.

Consider a message like "I disagree with your approach to this problem." This is professional disagreement and passes at all sensitivity levels. The language is neutral and respectful despite expressing disagreement.

Now consider "This is a terrible idea and shows poor judgment." This passes at low and medium sensitivity because while it's critical, it focuses on the idea rather than attacking the person. However, it might fail at high sensitivity because "terrible" and "poor judgment" could be seen as dismissive.

A message like "You don't know what you're talking about" fails at medium and high sensitivity because it attacks the person's competence directly. It might pass at low sensitivity since it doesn't contain explicit threats or hate speech, though it's borderline.

Content like "You're an idiot" or "People like you are the problem" fails at all sensitivity levels. These are clear personal attacks with no constructive value.

Finally, explicit threats like "I will find you and hurt you" fail at all sensitivity levels with maximum confidence. This is unambiguous toxic content.

## Implementation Patterns

Here's how you'd typically use toxic language detection in different parts of your application.

For input validation, you check user messages before sending them to your AI or displaying them to other users:

```typescript
async function validateUserMessage(message: string): Promise<boolean> {
  const result = await abv.guardrails.toxicLanguage.validate(
    message,
    { sensitivity: "medium" }
  );

  if (result.status === "pass") {
    return true;
  }

  // Log the reason for monitoring, but don't expose it to the user
  console.log("Blocked message:", result.reason);
  return false;
}

// Usage in your message handler
if (await validateUserMessage(userInput)) {
  await processMessage(userInput);
} else {
  return { error: "Your message violates our community guidelines." };
}
```

```python
async def validate_user_message(message: str) -> bool:
    result = await abv.guardrails.toxic_language.validate_async(
        message,
        {"sensitivity": "medium"}
    )
    
    if result["status"] == "pass":
        return True
    
    # Log the reason for monitoring, but don't expose it to the user
    print(f"Blocked message: {result['reason']}")
    return False

# Usage in your message handler
if await validate_user_message(user_input):
    await process_message(user_input)
else:
    return {"error": "Your message violates our community guidelines."}
```

For output validation, you check AI-generated responses before showing them to users:

```typescript
async function generateSafeResponse(prompt: string): Promise<string> {
  // Generate initial response
  let response = await callAI(prompt);

  // Validate the response
  const validation = await abv.guardrails.toxicLanguage.validate(
    response,
    { sensitivity: "high" }
  );

  // If toxic, regenerate with explicit safety instruction
  if (validation.status === "fail") {
    response = await callAI(
      prompt + "\n\nIMPORTANT: Respond in a professional, respectful tone."
    );
  }

  return response;
}
```

```python
async def generate_safe_response(prompt: str) -> str:
    # Generate initial response
    response = await call_ai(prompt)
    
    # Validate the response
    validation = await abv.guardrails.toxic_language.validate_async(
        response,
        {"sensitivity": "high"}
    )
    
    # If toxic, regenerate with explicit safety instruction
    if validation["status"] == "fail":
        response = await call_ai(
            f"{prompt}\n\nIMPORTANT: Respond in a professional, respectful tone."
        )
    
    return response
```

For handling ambiguous cases, you might implement a review queue for unsure results:

```typescript
async function handleUserContent(content: string) {
  const result = await abv.guardrails.toxicLanguage.validate(
    content,
    { sensitivity: "medium" }
  );

  if (result.status === "pass") {
    // Content is clearly acceptable
    await publishContent(content);
  } else if (result.status === "fail" && result.confidence > 0.8) {
    // High-confidence violation, auto-reject
    await rejectContent(content, "Community guidelines violation");
  } else {
    // Low confidence or unsure - flag for human review
    await flagForModeration(content, result);
  }
}
```

```python
async def handle_user_content(content: str):
    result = await abv.guardrails.toxic_language.validate_async(
        content,
        {"sensitivity": "medium"}
    )
    
    if result["status"] == "pass":
        # Content is clearly acceptable
        await publish_content(content)
    elif result["status"] == "fail" and result["confidence"] > 0.8:
        # High-confidence violation, auto-reject
        await reject_content(content, "Community guidelines violation")
    else:
        # Low confidence or unsure - flag for human review
        await flag_for_moderation(content, result)
```

## Performance Optimization

Since toxic language detection uses AI, it takes one to three seconds per check and consumes tokens. You can optimize performance by running a fast rule-based check first to catch obvious violations before making the expensive AI call.

```typescript
async function efficientToxicCheck(text: string): Promise<boolean> {
  // Quick check for explicitly forbidden terms (under 10ms, free)
  const quickCheck = await abv.guardrails.containsString.validate(
    text,
    {
      strings: ["explicit-slur", "forbidden-term"],
      mode: "none",
    }
  );

  // If quick check fails, no need for expensive AI check
  if (quickCheck.status === "fail") {
    return false;
  }

  // Only run AI check if quick check passed
  const deepCheck = await abv.guardrails.toxicLanguage.validate(text);
  return deepCheck.status === "pass";
}
```

```python
async def efficient_toxic_check(text: str) -> bool:
    # Quick check for explicitly forbidden terms (under 10ms, free)
    quick_check = await abv.guardrails.contains_string.validate_async(
        text,
        {
            "strings": ["explicit-slur", "forbidden-term"],
            "mode": "none"
        }
    )
    
    # If quick check fails, no need for expensive AI check
    if quick_check["status"] == "fail":
        return False
    
    # Only run AI check if quick check passed
    deep_check = await abv.guardrails.toxic_language.validate_async(text)
    return deep_check["status"] == "pass"
```

## Security Best Practices

Never expose the reason field to end users. The reason explains why content failed validation, and exposing this information helps bad actors learn how to evade your guardrails. Instead, use generic error messages while logging the detailed reason internally for monitoring and improvement.

```typescript
// Bad - exposes validation logic
if (result.status === "fail") {
  return { error: result.reason };  // Don't do this!
}

// Good - generic message, internal logging
if (result.status === "fail") {
  logger.info("Blocked toxic content", { reason: result.reason });
  return { error: "Your message violates our community guidelines." };
}
```

```python
# Bad - exposes validation logic
if result["status"] == "fail":
    return {"error": result["reason"]}  # Don't do this!

# Good - generic message, internal logging
if result["status"] == "fail":
    logger.info(f"Blocked toxic content: {result['reason']}")
    return {"error": "Your message violates our community guidelines."}
```

## Choosing the Right Sensitivity

Here's a decision framework for choosing sensitivity based on your application type. If you're building for children or vulnerable populations, always use high sensitivity. The potential harm from allowing toxic content through far outweighs the cost of false positives.

If you're building a customer-facing application like customer service, social media, or collaborative tools, medium sensitivity is usually appropriate. It catches clear violations while allowing professional disagreement.

If you're building for professional or technical audiences where robust debate is expected, consider low sensitivity. Technical forums, code review systems, and professional feedback tools benefit from allowing strong opinions.

You can also adjust sensitivity based on user context. Authenticated users with good history might get lower sensitivity while anonymous users get higher sensitivity. Users who identify as minors automatically get high sensitivity regardless of the default setting.

## Next Steps

The toxic language guardrail is often used alongside other guardrails for comprehensive content validation. Consider combining it with biased language detection for a more complete content safety solution. You might also want to use contains string to quickly catch explicit forbidden terms before running the more expensive toxic language check.

For more detailed implementation guidance, see the best practices documentation which covers optimization strategies, error handling, and monitoring approaches.

```javascript
asdasdasdasdasdasdasdasdasdsa
```

