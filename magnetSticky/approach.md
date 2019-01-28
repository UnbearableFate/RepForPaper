## defination of magnet and sticky

Measuring Contributor Retention and Attraction in Questions of Stack Cverflow

This section describes our measurements of personnel retention and attraction in the subjects discussed by the users of Stack Overflow. In this study, we use the Magnet and Sticky metrics defined by the Pew Research Center [26] for illustrating the migratory trends of citizens in the United States.

*The Pew Research Center report1 defines magnet states as those states where a large proportion of adults who live there have moved from another state. Thus, the magnet metric for a state is the proportion of adult residents of a state who were not born in the state. Furthermore, the report also defines sticky states as those states where a large proportion of adults who were born there continue to live there. Thus, the sticky metric for a state is the proportion of adult residents who were born in the state*

*These definitions are sound for a study of populations, where a single adult can only occupy one state at a time.However, the definition cannot be applied directly to **the subjects discussed by the users of Stack Overflow** where **a user can ask or answer questions in several subjects at the same time. **Therefore, we expand original definition to apply to **subjects in Stack Overflow** as follows:*

### **Subjects discussed in Stack Overflow**
Questions in Stack Overflow are composed of the content of the question, answers to the question and comments ,which are call Posts in the database of SOtenent. Each question have one or more tags that separate the question into different subjects. Simultaneously, Posts in a qustion have their own creater (For the content of question, one is the questioner, and for the answer, one is the respondent.)who is participant of the subjects of the question.we also define the acitivity of asking or answering questions in some subject as disscussion of the subject
For example, a classical questions in Stack overflow has three tags like \<java\>, apache and linux which is asked by user A and answered by user B, and C, so A ,B and C are  participants of subject java apache and linux, by the way , We will discuss the participation of specific subjects in several major categories, so the three subjects java apache and linux are also belong to  major categories Program language , Framework and OS.

### **Magnet**
*Magnet projects are those that attract a large proportion of new users. Thus, we calculate the magnetism of a subject as the proportion of users who ask or answer during the time period under research to all new users who resigster their account at the year.*

### **Sticky**
*Sticky projects are those where a large proportion of the contributors will keep discussing in the time period the following and under research. Thus, we calculate the stickiness of a subject as the proportion of the users who discuss within the subject in the time period under research to who have also discuss in the following time period.*

*Figure 1 shows an example of our definition. In this example, we examine the 2017 time period. There are five users (A, B, C, D and E) and two subjects in the same major category (1 and 2). To calculate the magnet metric, we observe that there are three new users who register his/her account in 2012  (B, C and D), and two of them discuss in subject 1 (B and C), while one user (D) discuss in subject 2. In this case, Magnet value of project 1 is 2/3 and project 2 is 1/3.*
*To calculate the sticky metric, in subject 1, three users participate in the discussion in 2011 (A, B and C) two of them also  participate in the discussionin 2012 (A and B). Hence, the sticky value of project 1 is 2/3. In subject 2, one user participate in the discussion of the subject in 2011 (D) and two users (D and E) participate in the discussion in 2012. However, the sticky metric only considers the number of users who participate in the discussion of the subjects in the studied time period and the next one. Hence, Sticky value of subject 2 is not 2/1, but rather 1/1.*