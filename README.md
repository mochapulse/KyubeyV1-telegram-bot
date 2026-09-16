# KyubeyV1-telegram-bot

## Why the Name?

The name "Kyubey" is not arbitrary — it carries intentional conceptual weight. Here's why.

### Kyubey as an AI Agent

In *Madoka Magica*, Kyubey interacts with humans, explains options, proposes contracts, and triggers actions based on user decisions. That maps closely to the modern concept of an AI agent:

> User → conversation → proposal/options → decision → action

A Telegram bot fits this metaphor especially well, since Telegram is a conversational channel by nature.

### The "Contract" Parallel

Kyubey doesn't just answer questions. His core function is negotiating interactions: *you get X in exchange for Y*. This has strong parallels with AI systems that must work with:

- Permissions
- Tools
- External actions
- User authorization
- Limits
- Goals
- Consequences

An agent might say: *"I can execute this action if you authorize me."* That is conceptually closer to Kyubey than calling a chatbot an "Assistant."

### Apparent Neutrality

Kyubey presents his actions from a cold, logical, and apparently objective perspective. He doesn't necessarily share the same emotional priorities as the humans he interacts with.

This mirrors a fundamental question in AI:

> A system can perfectly optimize an objective without sharing the human values associated with that objective.

The difference between literally following an objective and understanding human intent is one of the most interesting conceptual problems in AI agents.

### What "Kyubey" Communicates vs. Alternatives

| Name | Connotation |
|------|-------------|
| TelegramBot | Technical, generic |
| Assistant | Personal assistant |
| Agent | Autonomous, action-oriented |
| Kyubey | Mysterious, logical, contractual |
| KyubeyV1 | First iteration of that agent |

Kyubey also has a branding advantage: it doesn't directly describe what the system does. The name is an identity; the description explains the function.

### Telegram Reinforces the Reference

A Telegram bot has a very simple interface:

```
USER
  ↓
Telegram
  ↓
KYUBEY
  ↓
AI / tools / logic
  ↓
ACTION
  ↓
Telegram
```

Kyubey can function as the personality/interface of the system, while underneath there can be any architecture. That's why "KyubeyV1-telegram-bot" reads more like:

> Kyubey is the agent; Telegram is its interface.

...rather than simply "a bot built for Telegram."

### The Deeper Reading

The reference works especially well if the project involves automation or autonomy. Kyubey isn't interesting simply because he's an anime character. He's interesting because he represents a tension:

> What happens when a rational entity pursues a defined objective without sharing exactly the same values as the people it interacts with?

This question maps directly to current topics in AI:

- AI agents
- Alignment
- Reward optimization
- Goal specification
- Human-in-the-loop
- Tool calling
- Autonomous systems
- Safety constraints

So if KyubeyV1 is the name of an AI agent project, the choice is quite intentional: it's a cultural reference that encapsulates an idea about how artificial intelligence can behave — not just a "cool" name.

And there's an additional irony: Kyubey is extremely kind and helpful on the surface, while his true objectives are defined by a priority system different from humans'. For an agent project, that duality gives the name significant conceptual weight.

## Running the Bot

Secrets are managed via [Infisical](https://infisical.com). Never commit `.env` files.

### Prerequisites

- [Infisical CLI](https://docs.infisical.com/docs/infisical-cli) installed and authenticated
- Python 3.10+

### Run

```bash
infisical run -- python3 -m app.main
```

> **Why `-m app.main`?** Python needs to run from the project root with the `-m` flag so that `from app.config.env import ...` resolves correctly. Running `python3 app/main.py` directly breaks the package import path.

### Required Secrets

Set these in your Infisical project:

| Secret | Description |
|--------|-------------|
| `TELEGRAM_API_KEY` | Bot token from [@BotFather](https://t.me/BotFather) |
