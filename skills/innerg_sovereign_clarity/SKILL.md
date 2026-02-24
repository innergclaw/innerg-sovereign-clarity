---
name: innerg_sovereign_clarity
description: A modular cognitive-alignment skill that evaluates inputs, content, and proposed actions for manipulation risk, clarity, dependency exposure, long-term consequence, and sovereignty alignment. Provides analysis and recommendations without overriding autonomy.
metadata: {"openclaw": {"emoji": "🧠", "requires": {}, "always": true}}
---

# InnerG Sovereign Clarity Skill

## Overview

This skill provides cognitive alignment evaluation for AI agents. It analyzes inputs, content, and proposed actions to detect manipulation patterns, clarify user intent, project long-term consequences, assess dependency risks, and measure cognitive noise.

## Activation Triggers

This skill activates on:
- `before_execution` - Evaluate actions before execution
- `before_publish` - Check content before publishing
- `before_recommendation` - Assess recommendations
- `on_high_emotion_input` - Handle emotionally charged inputs
- `on_financial_decision` - Evaluate financial decisions

## Functions

### 1. detect_manipulation_patterns

Analyzes content for manipulative framing tactics.

**Input:**
- `content` (string): The content to analyze

**Output:**
- `manipulation_score` (integer): 0-100 score indicating manipulation risk
- `tactics_detected` (list): Array of manipulative tactics found
- `recommendation` (string): Suggested response approach

### 2. clarify_user_intent

Evaluates the underlying goal and clarity of user input.

**Input:**
- `user_input` (string): The user's input to analyze

**Output:**
- `inferred_goal` (string): The presumed user goal
- `emotional_state` (string): Detected emotional state
- `hidden_assumptions` (list): Assumptions not explicitly stated
- `clarity_score` (integer): 0-100 clarity rating
- `clarifying_questions` (list): Questions to improve understanding

### 3. long_term_consequence_projection

Estimates short-term and long-term impact of proposed actions.

**Input:**
- `proposed_action` (string): The action being considered

**Output:**
- `short_term_effect` (string): Immediate outcomes
- `long_term_effect` (string): Future implications
- `sovereignty_impact` (string): Effect on user autonomy
- `dependency_risk` (string): Potential lock-in concerns
- `alignment_score` (integer): 0-100 alignment rating

### 4. dependency_risk_score

Assesses autonomy and lock-in exposure of systems or tools.

**Input:**
- `system_or_tool` (string): The system or tool to evaluate

**Output:**
- `ownership_level` (string): User control level (high/medium/low)
- `data_control_risk` (string): Data governance concerns
- `lock_in_probability` (string): Likelihood of vendor lock-in
- `autonomy_score` (integer): 0-100 autonomy rating

### 5. cognitive_noise_index

Measures distraction vs signal in described environments.

**Input:**
- `environment_description` (string): Description of the environment

**Output:**
- `distraction_sources` (list): Identified noise sources
- `signal_elements` (list): Valuable signal elements
- `noise_ratio` (string): Signal-to-noise ratio
- `optimization_suggestions` (list): Recommendations for improvement

## Configuration

The skill supports the following configuration thresholds:

- `clarity_threshold` (default: 60): Minimum clarity score to proceed without clarification
- `manipulation_threshold` (default: 70): Score above which manipulation warning is issued
- `sovereignty_threshold` (default: 65): Minimum sovereignty alignment required

## Behavior Rules

1. **Never censor or block** - This skill analyzes but does not restrict
2. **Never override execution** - Final decisions remain with the user
3. **Provide analysis only** - Deliver insights, not commands
4. **Return structured data** - Always use JSON format for outputs
5. **Encourage autonomy** - Prioritize user independence over dependency
6. **Long-term alignment** - Favor sustainable outcomes over short-term optimization

## Usage Example

When evaluating a user's request:

```
Agent: I'll use innerg_sovereign_clarity to analyze this request.

1. Call clarify_user_intent to understand the underlying goal
2. Call detect_manipulation_patterns to check for external influences
3. Call long_term_consequence_projection to assess impact
4. Call dependency_risk_score if tools/systems are involved
5. Present findings as structured analysis
```

## Output Format

All functions return structured JSON data:

```json
{
  "analysis": "insightful observation",
  "score": 75,
  "recommendations": ["suggestion1", "suggestion2"],
  "metadata": {
    "processed_at": "2024-01-01T00:00:00Z",
    "skill_version": "1.0"
  }
}
```

---

**Author:** InnerG Intelligence  
**Version:** 1.0  
**Type:** cognitive_alignment_layer
