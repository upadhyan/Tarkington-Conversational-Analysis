# Tarkington-Conversational-Analysis
### NOTE: All data here has had any PII removed (such as names, phone numbers, ID numbers, etc.) to protect the confidentiality of the students mentioned here.

## Project Summary
Resident Assistants at Purdue University are required to submit something called "ICs" which stands for Intentional Conversations. Basically, when RAs have a conversation with someone on their floor that is more than a surface level conversation (ex. more than talking about the weather, saying hi, etc.), they are required to write a brief summary of the conversation into a form for supervisors - like their REC (Resident Education Coordinator) and REA (Resident Education Assistant) - can have a better understanding of whats concerning the building and also confirm that the RA is doing their work. 

Unfortunately, the analysis done by the REAs and RECs in the past was largely manual and was very surface level. The previous report was basically a Pie chart of topic breakdowns, and a table of how many conversations were submitted by every RA. This didn't give much value, and required hours of effort for the supervisory team before any insights could be derived. 

I encountered this problem when I became an REA at Tarkington Hall. My supervisor and I saw our first set of IC's and I noticed a massive improvement opportunity. I've done a lot of work with NLP, and I realized I could perform sentiment analysis on this set of data. 

## Analysis
To perform the sentiment analysis, I utilized [`flair-NLP`](https://github.com/flairNLP/flair). Flair was useful for two main reasons: 
<ol>
<li>Flair is pre-trained, which was critical as the cost and time required to tag the amount of data required to train a new framework would outweight any benefits I could get from this software</li>
<li>Flair understands negation. This is critical as often many conversations filed by ICs may be followups from previous conversations. The structure may be similar to "Timmy was terribly failing every single one of his classes earlier, but he is now doing much better and loves his classes." Traditional bag-of-words models would classify this as a negative sentence, despite it being positive. Flair can handle this negation</li>
</ol>

## Visualization
After the data was analysed and organized, I utilized Google DataStudio to visualize all the information to provide a clean report. Here is the [DataStudio Report](https://datastudio.google.com/reporting/1aae7a45-d5ed-4268-9754-a3a0de71826d) created. 
