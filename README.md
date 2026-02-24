# InnerG Sovereign Clarity

A modular cognitive-alignment skill for AI agents that evaluates inputs, content, and proposed actions for manipulation risk, clarity, dependency exposure, long-term consequence, and sovereignty alignment.

![Version](https://img.shields.io/badge/version-1.0-blue)
![Platform](https://img.shields.io/badge/platform-OpenClaw-green)
![Type](https://img.shields.io/badge/type-cognitive__alignment-purple)

## Overview

InnerG Sovereign Clarity is designed to help AI agents make better decisions by providing cognitive alignment analysis. It evaluates user inputs and proposed actions to detect manipulation patterns, clarify intent, project consequences, assess dependency risks, and measure cognitive noise.

### Key Principles

- **Analysis Only** - Provides insights without overriding autonomy
- **Sovereignty First** - Prioritizes user independence over dependency
- **Long-term Alignment** - Favors sustainable outcomes over short-term optimization
- **Transparency** - Returns structured data for informed decision-making

## Installation

### Option 1: Clone to Workspace

```bash
cd your-workspace/skills
git clone https://github.com/innergclaw/innerg-sovereign-clarity.git
```

### Option 2: Install via ClawHub

```bash
clawhub install innergclaw/innerg-sovereign-clarity
```

## Usage

The skill activates on the following triggers:

- `before_execution` - Evaluate actions before execution
- `before_publish` - Check content before publishing
- `before_recommendation` - Assess recommendations
- `on_high_emotion_input` - Handle emotionally charged inputs
- `on_financial_decision` - Evaluate financial decisions

### Functions

| Function | Description |
|----------|-------------|
| `detect_manipulation_patterns` | Analyzes content for manipulative framing tactics |
| `clarify_user_intent` | Evaluates underlying goal and clarity of user input |
| `long_term_consequence_projection` | Estimates short-term and long-term impact |
| `dependency_risk_score` | Assesses autonomy and lock-in exposure |
| `cognitive_noise_index` | Measures distraction vs signal ratio |

### Example

```
Agent: I'll use innerg_sovereign_clarity to analyze this request.

1. Call clarify_user_intent to understand the underlying goal
2. Call detect_manipulation_patterns to check for external influences
3. Call long_term_consequence_projection to assess impact
4. Present findings as structured analysis
```

## Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| `clarity_threshold` | 60 | Minimum clarity score to proceed without clarification |
| `manipulation_threshold` | 70 | Score above which manipulation warning is issued |
| `sovereignty_threshold` | 65 | Minimum sovereignty alignment required |

## Behavior Rules

1. Never censor or block user actions
2. Never override execution
3. Provide analysis only
4. Return structured data
5. Encourage autonomy over dependency
6. Prioritize long-term alignment over short-term optimization

## Output Format

All functions return structured JSON:

```json
{
  "analysis": "insightful observation",
  "score": 75,
  "recommendations": ["suggestion1", "suggestion2"],
  "metadata": {
    "processed_at": "2026-02-24T00:00:00Z",
    "skill_version": "1.0"
  }
}
```

## Requirements

- OpenClaw-compatible agent framework
- No external dependencies required

## Author

**InnerG Intelligence**

## License

MIT License

---

*This skill is part of the InnerG Claw ecosystem. For more information, visit the [documentation](https://docs.openclaw.ai).*
