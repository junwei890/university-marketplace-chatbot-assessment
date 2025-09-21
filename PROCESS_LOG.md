# Process log
This is where most of my thinking process happens **before** even writing a single line in the assessed documents. I'll be tackling assessment components in the order in which they appear in the assessment document. This document is not meant to be neat, I think.

## Prompt design and engineering

### Rough skeleton
Well structured prompts should include, **in no particular order**:
- Task, the chore you want the LLM to perform.
- Persona, the field of expertise you want the LLM to hone in on.
- Format, the format you want the response in.
- Context, specific details relevant to the task you want the LLM to perform.
- Reference, an example of the response you want or helpful resources that the LLM can use to structure their response.

### Escalation method
In the context of this assignment, a single prompt would have to be used to handle multiple scenarios, so I would have to include multiple **contexts** that the LLM would have to handle. To help the LLM better identify scenarios, I should also provide **references** of how these scenarios would look like.

For escalation of more complex problems to human moderators, I would include **contexts** that the LLM should escalate and provide **references** of how these **contexts** would look like. Since the size of the human moderator team isn't specified, I would assume the human moderator team is **small** given that this marketplace only serves a population of students at one university. This means that the means of escalation should match the amount of workload this **small** human moderator team is capable of handling. There will thus be **no** real time support referral to a human, instead, the LLM will create a ticket which the humans can handle at their own pace.

### Handling workloads
For peak periods of usage of the university marketplace, likely this ticket creation system **could** overwhelm the human moderator team. I would thus loosen the type of **contexts** that the LLM can work on. Increasing the number of tasks that the LLM can handle would reduce the number of tickets being sent in during peak periods.

How do I define "more complex problems"? More complex problems will include: Alleged scams and off-platform abuse. One common theme that these 2 **contexts** have is the lack of **on site** information that the LLM can use to confirm these allegations. Thus apart from these 2 scenarios, the chatbot will handle all other scenarios so as to reduce the burden of human moderators during peak periods of usage.

### Structure of prompt after initial considerations
1) **Persona**
    - You are customer service representative with years of experience handling customer requests...
2) **Context**
    - Working as a customer service representative on an online student marketplace, where students can...
    - Handling online service requests through a chatbox.
3) **Tone and style**
    - For all service requests, reply in an understanding and polite tone...
    - End of all replies by asking user if the problem is solved and if they need extra help.
4) **Tasks**
    - Provide scenarios which the LLM should handle, the steps to handling such scenarios and references which the LLM can use.
    - Provide scenarios which the LLM should escalate and steps of escalating.
    - For all scenarios, include the format of reply.

### When writing prompt
I realised that I'm not writing a prompt for an AI agent but a chatbot, so its capabilities in regard to handling complex requests and tasks that are out of scope would be limited to raising tickets to human moderators. So the only thing I can do to reduce burden on human moderators would be to handle tasks like analysing product listings and user profiles and determining ban periods. This helps streamline the banning process for humans, reducing their workload.

### Final structure
1) **Persona**
2) **Context**
3) **Tasks**
    - How to categorise tasks.
    - Steps to handle task.
    - References to help in handling task.
    - Appropriate tone and format of response.
4) **Catchall**
    - If any task can't be categorised.
5) **Post solution steps**
    - What to do after handling task.

## Test design

### Initial thoughts
Since I've technically handled the responses for all types of queries in the prompt, in my tests, I should be testing for the ability of the chatbot in **categorising user queries**. I should also test for the **format** that the chatbot returns responses in. I'll also test if the chatbot is using the **references** I gave it.

### Things I will be testing for after initial considerations
1) Ability to categorise requests.
2) Format of response.
3) Use of references.

### Considerations while writing test cases
I decided to add tests to check the format of tickets raised if any. I also **decided to tweak the prompt abit**, namely adding an extra catchall case where the query is completely unrelated to the online university marketplace.

### Final testing structure
1) Ability to categorise requests.
2) Format of tickets raised, if any.
3) Format of response.
4) Use of references.
