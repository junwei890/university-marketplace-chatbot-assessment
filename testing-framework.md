# Testing framework
In order to test my chatbot, I had to identify potential points of failure. The points of failure identified include: Failure to categorise user inputs, incorrect escalation workflows and incorrect tone and style of response.

Identifying the category of a user query is important as in accordance to my prompt, it directly affects escalation workflows. Incorrect categorisation could lead to unnecessary escalation, increaing the burden of human moderators. To test the chatbot's ability to categorise user queries, I included a field named "category" that the chatbot has to correctly identify in order to pass the test case.

Getting escalation workflows right is another important component of my chatbot. A robust escalation workflow would provide human moderators with perfect information, allowing them to handle escalated user queries more efficiently. A robust escalation workflow would also help human moderators prioritise more urgent user queries, improving overall customer service. To test my chatbot's ability to correctly raise a ticket, I included a field name "ticket_details" that consists of subfields "priority" and "body", that the chatbot has to correctly infer and fill out (according to the reference I gave it in the prompt) in order to pass the test case.

Arguably the most important aspect of a chatbot is the user experience, thus responses should be crafted with the appropriate tone and style to match the situation. In my tests, I included "tone" and "response_body" fields in the "response_details" field to test for expected words and sentences that should appear in the response. The response by the chatbot has to have the expected words and sentences in order to pass the test case.

I did not test for edge cases because I included multiple catchall scenarios in my prompt. Thus, my test cases focused solely on the quality and correctness of responses from my chatbot.
