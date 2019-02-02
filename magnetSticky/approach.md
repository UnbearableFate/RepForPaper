## defination of magnet and sticky

Measuring Contributor Retention and Attraction in Questions of Stack Cverflow

This section describes how we measure the appeal and adhesion of users who participate in disssion of different topics on Stack Overflow.In this study, we use the Magnet and Sticky metrics defined by the Pew Research Center [26] for illustrating the migratory trends of citizens in the United States.

The Pew Research Center report defines magnet state as a state that the majority of residents living in the state are not born in this state. Thus, the magnet metric for a state is the proportion of adult residents of a state who were not born in the state. Additionally, the report also defines the sticky state as a state that the majority of the state’s adult residents were born and have been living in the state. Thus, the sticky metric for a state is the proportion of adult residents who were born in the state

These definitions are sound for a study of populations, where a single adult can only occupy one state at a time. However, the definition cannot be applied directly to the topics discussed by the users of Stack Overflow where a user can ask or answer questions in several topics at the same time. Therefore, we expand original definition to apply to topics in Stack Overflow as follows:*

### **Topics discussed in Stack Overflow**
Questions in Stack Overflow are composed of the content of the question, answers to the question and comments ,which are call Posts in the database of SOtenent. Each question have one or more tags that separate the question into different topics. Simultaneously, Posts in a qustion have their own creater (For the content of question, one is the questioner, and for the answer, one is the respondent.)who is participant of the topics of the question.we also define the acitivity of asking or answering questions in some topic as disscussion of the topic
For example, a classical questions in Stack overflow has three tags like \<java\>, apache and linux which is asked by user A and answered by user B, and C, so A ,B and C are  participants of topic java apache and linux, by the way , We will discuss the participation of specific topics in several major categories(e.g C++ and program language), so the three topics java apache and linux are also belong to  major categories Program language , Framework and OS.

### **Magnet**
Magnets are those that attract a large proportion of new users. Thus, we calculate the magnetism of a topic as the proportion of users who ask or answer during the time period under research to all new users who resigster their account at the year.

### **Sticky**
*Sticky topics are those where a large proportion of the users will keep participating in discussion in the time period under research and the following. Therefore, we calculate the stickiness of a topic as the proportion of the users who discuss within the topic in the time period under research to who have also discuss in the following time period.

**Figure 1 here**

Let us take the survey of magnet and sticky of some topics belong to a major category as a exmaple . There are 6 questions (a,b, c, d, e, f) and 7 users (A, B, C, D, E, F, G), the Last Activity Date of question a, b, c is during 2017 and question d ,e, f is during 2018. the register date of user A, B, C, D is during 2017 and  the register date of user E, F, G is during 2018.

Questions have different tags. We merge tags belonging to the same topic into one topic ,for example tag "python-2.7" and tag "python-3.6" are merged into topic "python". so we get 3 topics in this case.

To calculate the magnet metric, we observe that there are four new users who register his/her account in 2017  (A, B, C and D), and all of them discuss in topic 1, while two users (BC) discuss in topic 2 and two users participate in the disccusion of topic 3. In this case, Magnet value of topic 1 in 2017 is 4/4 , topic 2 is 2/4 and topic is 2/4. 

To calculate the sticky metric, on topic 1, there are three users participate in the discussion in 2017 (A, B and C) but only one of them also  participate in the discussion in 2018 (A). Hence, the sticky value of project 1 is 1/4 . on topic 2, there are 2 users participate in the discussion in 2017 (B and C) but only one of them also  participate in the discussion in 2018 (B). Even though new users E F G participate in the discussion in 2018, we still calculate the value of sticky as 1/2 .For the same reason, the sticky of topic 3 is 2/2 in 2018

# 3 Database
In this paper, we anlyze the Stack Overflow dataset provided by [Sebastian Baltes ->SOTorrent: Reconstructing and Analyzing the Evolution of Stack Overflow Posts.] called SOTorrent. 
SOTorrent is “an open dataset based on the official SO data dump. SOTorrent provides access to the version history of SO content at the level of whole posts and individual text or code blocks. It connects SO posts to other platforms by aggregating URLs from text blocks and by collecting references from GitHub files to SO posts.”
The dataset includes 20 different table which store not only data from official SO data dump but also data extracted from original data dump.
however , in this paper , we only anlyze the data from table "Posts" which includes about 42 million posts from Stack overflow and table "Users" where there are about 9 million rows of user information and pay attation to user , tag and time informaiton of questions
In this paper, we consider a user to be one who ask or answer questions in Stack Overflow, Those who comment or like/unlike on questions or answers are not counted in the statistics.

# 5 Conclusion
Whether it's a programming language or a program framework or an operating system, keeping the community alive and attracting more people to participate in discussions is critical to its development.Especially on the stack overflow, the world's largest program Q&A platform, having more questions and answers on a topic means that customers of the product are more likely to solve their own problems, which is even more tedious than that developers rack their brains to write a lengthy development document or Q&A
This paper applied the magnet and sticky population concepts to a set of topics in Stack Overflow. We find that:
1. The number of topics that people participate in is exploding with the development and popularity of computer technology.Even the most popular themes can't attract the high percentage of people involved in the discussion like what they did ten years ago.
2. Under their respective major categories, the most popular topics are still very popular after ten years, and only a small number of languages or frameworks can stand out and become one of the most popular topics.
3. This research can provide some reference for enterprises to choose their own main technology stack, and can also be used as a reference for computer science students to learn new technologies, because it (1)predicts the trend of computer technology in the next few years, (2)points out which technologies are easier to access and the questions can be easier to get answers to.