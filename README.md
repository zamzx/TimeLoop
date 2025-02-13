# TimeLoop
TimeLoop is a simple python and Ollama project that iterates a prompt for a given amount of time. 

Notes on using TimeLoop. 

t = Timer(400, timeout) sets the loops run length in seconds. The loop is split into two functions, process_response calls the meta-validation and then it calls the llm_response for the next part in the story. It outputs to the console as it writes, and then dumps the full text (full_story) after the timer runs out.

***anyway post the stuff you generate in the issues***


I find it useful for getting 'MOAR' from LLM's in a single attempt. Also for writing NSFW content.  Make sure you have a custom system message set.

Depending on settings, I've gotten 10+ iterations of the loop. Sometimes 8+ pages of continuous plot. 
Telling it not to discuss or ask questiosn can keep it focused on writing and not self-talking.

Includes @bluecow009's superprompt which uses a lot of context length, but adds some intriguing reasoning. Again, turn on/off to see different results. 

Version 1 does not include a RAG. You can clearly see when the context size is filled by the LLM. 
Turning off the meta validation loop will give you a larger context size. Play with it to see if it'se helping or hurting your output. 

Ideas Coming for Version 2 -  I'd like to include statistical logging to track how different settings results in different complexity/connections. Visual connections graph. 

Playing with RAG's as well, but need more tinkering to make worthwhile. 

Adding an online loop for researching might be interesting, to see how it might influence writing as well. (Check online for ideas, details, etc) Could be a tool call. 

