---
layout: essay
type: essay
title: "Am I dumb?"
# All dates must be YYYY-MM-DD format!
date: 2023-09-05
published: true
labels:
  - Software Engineering
  - Learning
---
There are moments in our lives when we must seek assistance from others, particularly in this industry where mastering everything can be challenging. Consequently, asking questions is a crucial technique for finding the answers we need. However, the key question is: How can we ask questions in a manner that ensures immediate and effective answers? Eric Raymond has offered guidelines for this, which he refers to as "smart" questions. In my view, questions should not be classified as "smart" or "dumb," but rather their clarity and quality are the significant factors to consider. To further illustrate this idea, let’s take a look at questions on StackOverflow.
	

In this example, I consider this as a good question to ask because it provides sufficient information for people to figure out his difficulty. The following content is the question: 

```
Q: How to implement soft assertions in Cypress and stop execution on failure?
I installed the cypress-soft-assertions package with npm i -D cypress-soft-assertions.
2. In my test code, I have a method validateElementVisibility where I want to perform a soft assertion on element visibility:
validateElementVisibility(element, logMsg) {
    this.logger.log(logMsg);
    element.beter('be.visible'); // There's a typo here: it should be 'better' instead of 'beter'.
}

https://stackoverflow.com/questions/77044385/how-to-implement-soft-assertions-in-cypress-and-stop-execution-on-failure
```

In this question, the user has provided a comprehensive description of the entire process they followed, starting from their initial actions and continuing up to the point where they encountered a problem. This detailed account makes it easier for experts to replicate the code and identify the specific issue. Consequently, the question was answered within a day.
	
	

Now let’s look at a bad example:

```
I want to launch Android app with particular activity. Appium have 'start_activity' function, but it's deprecated. Instead of it offered to use 'mobile: startActivity' extension, but I can't understand how. I am newby in coding and realy appreciate any help.
Googling and Appium documentation reading not helped.

https://stackoverflow.com/questions/77050202/how-can-i-start-android-app-activity-using-appium-python
```

In this example, the user merely outlines their desired outcome without providing any context regarding their efforts or initial results. This is considered a bad question because the user should  present their question in a way that allows others to understand what they can do to assist. Requesting code from others without offering any background information or showing an attempt at problem-solving makes it challenging to provide a meaningful response. Consequently, this question remains unanswered.

In conclusion, asking a good question requires you to have a solid understanding of your code's context and to provide a clear explanation along with background information about what you've done. By doing so, your question can be understood quickly and easily by others, leading to a more effective and timely solution.
 
