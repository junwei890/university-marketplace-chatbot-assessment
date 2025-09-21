# Intern take home assignment

## Introduction
This is the **systems design** of an AI chatbot for an online university marketplace, where students can buy, sell and trade items within their campus community.

The AI chatbot is capable of the following:
- Helping users navigate the marketplace.
- Resolving common issues faced by users.
- Streamlining enforcement of community guidelines for moderators.
- Escalating of complex problems to moderators.

## Method of review
To review each component, click on the various files associated with each component.

Here are the **quicklinks** to assessed components:
1) Prompt design and engineering
    - [Prompt](./prompt.md)
    - [Analysis](./prompt-analysis.md)
2) Test design
    - [Test cases](./test-cases.json)
    - [Framework](./testing-framework.md)
3) Automation and update process
    - [Update process](./update-process.md)
    - [Automation concept](./automation-concept/)
4) Marketplace domain knowledge
    - [Marketplace insights](./marketplace-insights.md)

## Assumptions made
These are **assumptions** I made regarding this assignment:
1) This chatbot is not an AI agent, it does not have access to the database nor does it have the ability to interact with the webpage.
2) There is a small moderator team behind this online university marketplace.

## Time breakdown
This is how long I took to complete each assessed component:
- Prompt design and engineering -> **2 hours**
- Test design -> **2 hours**
- Automation and update process -> **1 hour**
- Marketplace domain knowledge -> **15 minutes**

## Next steps
If this were a real project, these would be the **next steps** I would take:
1) Setup proper Continuous Integration, Continuous Deployment pipeline with Github Actions.
2) Code implementation of chatbot using the FastAPI framework, Gemini API and uv as my package manager.
3) Setup Dockerfile.
4) (Automatically) Deploy to GCP cloud run.

## Personal reflection
The most difficult part of this project for me was writing the **prompt**. Though the industry standard prompt framework was quite straightforward (Task, Context, Reference, Evaluate, Iterate), implementing it was quite the task. I didn't want any part of the response to be left to chance so I had to be as specific and as helpful (by providing several references) to the LLM as possible in my prompt. It took me multiple rounds of iterating with various LLMs to find the best prompts to various mock user queries, but I finally settled on the prompt that you see in [prompt.md](./prompt.md).
