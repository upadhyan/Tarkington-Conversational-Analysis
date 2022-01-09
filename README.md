<h1>Tarkington-Conversational-Analysis</h1>
<h3> NOTE: All data here has had any PII removed (such as names, phone numbers, ID numbers, etc.) to protect the confidentiality of the students mentioned.</h3>

<h2> Project Summary</h2>
<p>Resident Assistants at Purdue University are required to submit something called "ICs" which stands for Intentional Conversations. Basically, when RAs have a conversation with someone on their floor that is more than a surface level conversation (ex. more than talking about the weather, saying hi, etc.), they are required to write a brief summary of the conversation into a form for supervisors - like their REC (Resident Education Coordinator) and REA (Resident Education Assistant) - can have a better understanding of whats concerning the building and also confirm that the RA is doing their work. </p>

<p>Unfortunately, the analysis done by the REAs and RECs in the past was largely manual and was very surface level. The previous report was basically a Pie chart of topic breakdowns, and a table of how many conversations were submitted by every RA. This didn't give much value, and required hours of effort for the supervisory team before any insights could be derived.</p>

<p>I encountered this problem when I became an REA at Tarkington Hall. My supervisor and I saw our first set of IC's and I noticed a massive improvement opportunity. I've done a lot of work with NLP, and I realized I could perform sentiment analysis on this set of data.</p>

<h2>Goals</h2>
<p>The primary goals for this project were to:
<ol>
  <li>Make it easy for RECs to understand what topics residents are worried about in the building so they can create relevant events and provide targeted resources to students</li>
  <li>Understand which floors in the building are feeling unhappy so the REC and REA can support the RA in charge of the floor appropriately</li>
  <li>Develop metrics to quantify the intentionality of an RA's engagement with their floor to drive </li>
  <li>Create a clear and consise report to answer the previous questions</li>
</ol></p>
<p>
My personal goals included: 
<ul>
  <li> Improving my ability to manipulate data in Python </li>
  <li> Apply skills I had picked up in previous experiences in a work setting </li>
  <li> Practice using Google DataStudio </li>
  <li> Explore the capabilities of Natural Language Processing and <a href = "https://github.com/flairNLP/flair">flair</a></li>
</ul>
</p>
<h2>Results</h2>
<p>The first result is values to understand RAs performance and how the floor is doing. Using outputs from flair, I was able to develop a "Happiness Score" metric to measure sentiment towards topics and sentiments of floors. Generally anything below a 50% happiness score is bad and action needs to be taken, anything between a 50% and 70% score is concerning but shouldn't be focused on if theres any red, and anything about a 70% is fine and normal. </p>
<p>I was also able to develop a "Quality Score" metric and a "Score Variance" metric to measure how detailed RAs make their conversations, and how varied their sentences are. A quality score below 70% is concerning and would indicate that the RA does not talk about much in their conversations and isn't gathering enough detail from their residents. A score variance of less than .05 indicates that the RAs conversations are very similar across all their residents, and the RA again is not being very intentional with their conversation. The code used to develop these metrics can be found in <a href = "https://github.com/upadhyan/Tarkington-Conversational-Analysis/blob/main/TarkICProcess.ipynb">the notebook attached to this repository.</a></p>
<p>
After the data was analysed and organized, I utilized Google DataStudio to visualize all the information to provide a clean report. Here is the [DataStudio Report](https://datastudio.google.com/reporting/1aae7a45-d5ed-4268-9754-a3a0de71826d) created. </p> 
