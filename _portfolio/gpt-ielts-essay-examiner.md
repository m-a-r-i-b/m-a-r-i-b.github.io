---
title: "GPT IELTS Essay Examiner"
excerpt: "Python, GTP, IELTS, Essay"
header:
  teaser: /assets/images/gpt-ielts-essay-examiner-1.jpg
date: "2023-06-17" 
---


<img src="{{ BASE_URL }}/assets/images/gpt-ielts-essay-examiner-1.jpg" alt="" class="full">


## Introduction
This was an attempt to create an AI based IELTs essay grading system. The project uses OpenAI's GPT-3-Turbo model and divides the scoring & feedback task into 4 sub tasks i.e.

-   Task Achievement
-   Coherence and Cohesion
-   Lexical Resources
-   Grammatical Range and Accuracy

It uses a separate prompt for each of the above tasks, specifically engineered to assess the respective criteria. Finally, outputing the combined result as an overall feedback and score. The results are okay-ish and could definitely benefit from few-shot examples if good quality samples become available.

Source code can be found in this [repository](https://github.com/m-a-r-i-b/gpt-ielts-essay-examiner).


## Solution Overview

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/gpt-ielts-examiner-2.png){: .align-center}


## Sample Result

### Input

#### Essay Title 
Doing an enjoyable activity with a child can develop better skills and more creativity than reading. To what extent do you agree? Use reasons and specific examples to explain your answer.

#### Essay Content
Parents throughout the world place spend time reading with their offspring to prepare them for school where their literacy skills are further developed; however, recent research suggests that focusing on reading at an early age can be detrimental, and participating in fun activities would be far more beneficial. I am a strong advocate of this approach, and the benefits of it will be covered in this essay.

A fundamental reason for this is that there is no biological age for reading, and pushing infants to acquire this skill before they are ready could have repercussions. For example, in the UK, many boys are reluctant readers, possibly because of being forced to read, and this turned them off reading. By focusing on other activities and developing other skills such as creativity and imagination, when they are ready to read, they usually acquire this skill rapidly.

In addition, the importance of encouraging creativity and developing a child's imagination must be acknowledged. Through play, youngsters develop social and cognitive skills, for example, they are more likely to learn vocabulary through context rather than learning it from a book.

Furthermore, play allows youngsters to mature emotionally, and gain self-confidence. There is no scientific research which suggests reading at a young age is essential for a child's development, moreover, evidence suggests the reverse is true. In Finland, early years' education focuses on playing.

Reading is only encouraged if a child shows an interest in developing this skill. This self-directed approach certainly does not result in Finnish school leavers falling behind their foreign counterparts. In fact, Finland was ranked the sixth-best in the world in terms of reading.

Despite being a supporter of this non-reading approach, I strongly recommend incorporating bedtime stories into a child's daily routine. However, reading as a regular daytime activity should be swapped for something which allows the child to develop other skills.


### Output

#### Overall Band Score

7

#### Detailed Feedback

Task Response: 

The essay addresses the prompt and presents a clear position that participating in fun activities is more beneficial than focusing on reading at an early age. The main ideas are relevant and well-developed, with specific examples to support the argument. The essay acknowledges the importance of encouraging creativity and developing a child's imagination through play, and the negative consequences of pushing infants to acquire reading skills before they are ready. The essay also provides evidence from Finland, where early years' education focuses on playing, and the country is ranked sixth-best in the world in terms of reading. However, the essay could benefit from more focus and precision in supporting ideas/material. The feedback also mentions that the essay is a strong advocate of the non-reading approach, but still recommends incorporating bedtime stories into a child's daily routine. Overall, the essay meets the criteria for Band 7. 

Coherence and Cohesion: 

The essay presents a clear overall progression and the ideas are logically organised. The use of cohesive devices is good, but there are some inaccuracies and overuse of certain words. For example, the word "skill" is used multiple times in the essay. The essay also lacks flexibility in the use of reference and substitution, resulting in some repetition. The paragraphing is generally effective, but the central topic is not always clear in some paragraphs. Overall, the essay presents a well-structured argument with some minor lapses in coherence and cohesion. 

Lexical Resource: 

The essay demonstrates a good range of vocabulary with appropriate usage. The writer has used a variety of words and phrases such as "fundamental reason", "repercussions", "self-directed approach", "cognitive skills", and "emotional maturity". However, there are a few instances of incorrect usage such as "place spend time" instead of "spend time" and "turned them off reading" instead of "turned them off from reading". 

The essay shows an awareness of style and collocation, but there are a few inappropriacies such as "pushing infants to acquire this skill" instead of "encouraging infants to acquire this skill". There are only a few errors in spelling and/or word formation, such as "leavers" instead of "graduates", but they do not detract from overall clarity.

Overall, the essay presents a well-structured argument with clear reasoning and specific examples. The writer acknowledges the importance of encouraging creativity and imagination in children and provides evidence to support their argument. The essay also shows an awareness of the opposing viewpoint and addresses it effectively. 

Grammatical range and Accuracy: 

The essay presents a clear argument and is well-structured with a good range of sentence structures. The writer uses a mix of simple and complex sentences, but there are a few errors in grammar and punctuation that could be improved. For example, in the sentence "Parents throughout the world place spend time reading with their offspring," there is an unnecessary word "place" that should be removed. However, the writer also uses more complex structures, such as "Through play, youngsters develop social and cognitive skills, for example, they are more likely to learn vocabulary through context rather than learning it from a book." The essay shows a good range of vocabulary, with words such as "repercussions," "self-directed," and "cognitive." The writer also provides specific examples to support their argument. Overall, the essay meets the criteria for a band 7, with a variety of complex structures used with some flexibility and accuracy, and occasional errors that do not impede communication. 


