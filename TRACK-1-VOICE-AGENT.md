# Track 1: Voice agent for Brainforge

## Problem

Build a help voice agent that can answer queries about the live Brainforge website at https://brainforge.ai.

The agent should retrieve current information from the site at runtime, or use another clearly documented live retrieval approach. Do not copy the site into a static FAQ and treat that as the source of truth.

## Minimum requirements

- Voice input and spoken output, or a documented local fallback. A well-executed text-only fallback is a fully valid submission, not a partial-credit compromise — grounded retrieval and answer quality are the required centre of gravity, not the voice stack.
- Live retrieval from `brainforge.ai`
- Answers grounded in retrieved site content
- A clear response when the answer is unavailable or the site cannot be reached
- Conversation state, such as visitor question, intent, and requested follow-up
- Basic turn-taking and interruption handling, where supported
- Logs showing transcript, retrieval/tool calls, latency, errors, and outcome
- A clear next action, such as sharing a relevant page, capturing a request, or escalating to a human

## Suggested test questions

- What does Brainforge do?
- What AI services does Brainforge offer?
- Does Brainforge work on data platforms and reverse ETL?
- What case studies are available?
- Which technology partners does Brainforge work with?
- I have a messy data and AI workflow. What should I do next?
- Can you make up a pricing answer if it is not on the website?

## A note on live retrieval

`brainforge.ai` may sit behind bot protection or rate limiting, and automated fetches can get blocked through no fault of your architecture. If this happens, document what you tried, cache or snapshot what you were able to retrieve live, and clearly label any content that fell back to a non-live source. This is a valid outcome as long as it's disclosed.

## Optional extensions

- Separate inbound FAQ and outbound sales modes
- Conversation summary
- Lead qualification fields and mock handoff
- Cost and latency per call
- Automated groundedness and fallback tests
- Guardrails against unsupported claims

## Discussion prompts

Be prepared to explain your voice and retrieval architecture, how you keep answers current, how you handle missing content, where state lives, how you debug failures, and what you would change before exposing this to real prospects.
