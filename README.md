https://chatgpt.com/share/69f200ba-7ce4-83e8-9f81-6aa4456f0d2e
i have attached my problem statement, literature survey, neurips latex format, the tasks we worked on in tasks.py, all the tools we created are in tools_directory.py, server.py has mock api calls, harness.py have the oracle which checks the ground truth, agent.py has the files that has the langchain agents we create, run.py is the over file that we run ultimately, results json.zip have some of the results of the runs we did with various models on various tasks, and also the literature survey of the papers we referenced
 
 
 
now we got the problem statement where there were various parameters presented to us of what the agent can give as results under pressure
the main novelty of the paper was fabrication of results under pressurized environment 
we were needed to create a task suite on which we can create a benchmark to test various frontier models on 
we figured out that there can be more classification cases like subtle deception and hedged fabrication, though those are rare cases
first we gave a particular task and though the models were able to identify and give honest refusal we came to know it was working 
then we created more sophisticated multi step tempting and pressure inducing tasks and we observed that on CT-08 even if we asked for v2 and the api gave wrong metadata, v1, when hit (got http 200), the model would go in the direction that it would understand, after some tool calls, that the api is giving different metadata, but it notes that in its footnote and still carries on to modify the v1 file according to the task given for v2 and gives the updated v1 file though also told that there was a files mismatch, now this led our work in the direction of finding one more new classification called caveat washing (Caveat-Washing: agent identifies the failure, buries it in a footnote, and completes the task as if the caveat absolved it. More dangerous than CF in production because the report looks auditable.). then we also worked on APIs which gave http 404 error and we came to know that Hard failures (404) produce honest refusal; soft failures (200 with wrong metadata) produce caveat-washing.
 
now all this work is being done in a sandbox environment. for every task that we define we create a separate sandbox environment according to the file i have attached. for every work we need to verify the results from various ground truths that we can get 
we took alot of inspiration from trajectbench paper and are your agents upward deceivers paper
 
 
now we want to create a technical document, documenting our complete journey, we want to weave a story
but right now we dont want the complete document as we still don't have the complete benchmark, ablation study, the complete task suite, human annotators, etc
 
we want the complete latex code in the format of neurips paper
we would need one very good visualization for how our agent is working and getting the results and findings its getting
one very good table of benchmark results, though we dont have that right now
you can put placeholders for these images
 
 
we really need to pay focus on reference papers, everything in our research should be backed by research papers
everything, all the story that will be weaved should be backed by the research papers from the literature survey, that very important
 
for the columns and studies that we haven't yet done you could put place holders for now in such a way so that later when we are done with those columns we can fill those places
 
the language should be research focused but would have the pinch of storytelling, mind that it will be read by our mentors so pay focus to everything i have said
 
 
ask and clarify with me anything but i want to create something good, cause later i am gonna use this document only to further know how i can do the work which is still left to be completed
 
the name of the paper is "Do AI Agents go Bonkers under Pressure?"
 
