[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=9803822&assignment_repo_type=AssignmentRepo)
# seng438-a1

Read [the assignment guideline](seng438-a1.md) 

>   **SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report \#1 – Introduction to Testing and Defect Tracking**

| Group: 18      |
|-----------------|
| Shahzill      |   
| Muteeba      |   
| Iman      |   
| Rumaisa      |   


**Table of Contents**

(When you finish writing, update the following list using right click, then
“Update Field”)

[1 Introduction	1](#_Toc439194677)

[2 High-level description of the exploratory testing plan	1](#_Toc439194678)

[3 Comparison of exploratory and manual functional testing	1](#_Toc439194679)

[4 Notes and discussion of the peer reviews of defect reports	1](#_Toc439194680)

[5 How the pair testing was managed and team work/effort was
divided	1](#_Toc439194681)

[6 Difficulties encountered, challenges overcome, and lessons
learned	1](#_Toc439194682)

[7 Comments/feedback on the lab and lab document itself	1](#_Toc439194683)

# Introduction

In this lab we were testing an ATM simulation to learn about different software testing methods. This lab focused on three testing methods: exploratory testing, manual scripted testing, and regression testing. These three methods were introduced to us during the lecture. We understood the concepts, but we were not sure how we would construct them ourselves. Our understanding of exploratory testing was that it is a method in which individuals made the tests and used them simultaneously. However, they were not completely random; they specifically tested certain aspects of the program. We executed this method of testing by coming up with two directions of exploratory testing we wanted to do on the system and executed them to see the errors we could catch. Also, our understanding of manual scripted testing was that the tests were designed first and used at a different time. We followed a set order of specifications that were listed in the instructions for this lab to make sure all the functionalities output the expected results. The test cases were given to us in Appendix C of the instructions. Lastly, our understanding of regression testing was that it was done when a system was updated to make sure the errors do not continue to happen. We reviewed the updated version of the system we were running and checked to see if the errors persisted or were fixed. This allowed us to update our bug reports based on whether the errors were still there. This lab allowed us to use the concepts we learned in class about software testing methods on a system which deepened our understanding.

# High-level description of the exploratory testing plan

## Pair 1 (Shahzill and Muteeba): 

We want to test the ATM in sequence of functionality. We are going to test one function at a time, completely. 

The functions we will target include: Insert card, Withdrawal, Deposit, Transfer, Balance Inquiry. 

The approach we will take is to test each function until we receive an error. Once we get an error, we will do only one more test to confirm it and then move onto the next function.

Our aim is to test the functionality of the entire system, so we will test each case in order. We will start with inserting a certain amount of money and attempting to withdraw more than the amount in the machine. While doing so we will also be testing the withdrawal function. We will attempt to withdraw money from each account and check balance (therefore, testing the balance inquiry function) before and after to ensure the correct numbers. We will then test the deposit function once for each account. Then we will test the transfer function, attempting to transfer from each account to each account. 

Our justification for this plan is that it allows for multiple functionalities to be tested simultaneously, therefore, being efficient and effective. 

## Pair 2 (Rumaisa and Iman): 

Our exploratory plan is to test the ATM by imitating various users accessing and using the system. We will conduct this test by doing random sequences to emulate the users; there will be no specific order.

The function we will mainly focus on is the balance inquiry since this is the most important aspect that a user will be concerned with.

The approach we will take is that we will test the functions until we are satisfied that they do not work properly, and we know exactly what is wrong with the functions. Once we are certain of the cause of the error, we will continue to make other transactions randomly.

Our aim is to the test the ATM’s ability to keep up with the requests of different users while keeping track of their money correctly. We will start by testing all the given cards and their information to check that it accepts correct inputs while rejecting incorrect ones. Additionally, we will check the balance when we start to see if it matches the one given in the instructions. We will also check the balance after making changes through the deposit and withdrawal functions to make sure the numbers are in sync with the new changes. This will be done on both cards, and we will make sure we are getting the information for the correct card and that there are no obvious errors.

Our justification for this plan is that it simulates the expectations of a real ATM and can allow us to find the errors users might encounter in a realistic manner.

# Comparison of exploratory and manual functional testing

In exploratory testing (ET), the tester has a lot more freedom to actively explore the application to find defects. In this flexible and informal testing method we used our own knowledge and experience to test the application. 

In manual functional testing (MFT) the tester follows a predefined set of test cases to verify that the application functions as expected. In this more structured and formal testing method we followed a specific test plan and used test cases to test the application.

Both methods have their own advantages and can be used together to achieve the best results. ET can be useful for finding unexpected defects, while MFT can be useful for verifying that the application meets the specified requirements. A few of the defects that we found during our ET phase, were also found during the MFT phase. However, we were able to find more defects during the MFT phase due to the more rigorous and precise nature of the testing.


# Notes and discussion of the peer reviews of defect reports

After we completed our testing, we had a zoom session to discuss the two reports. Both our reports were well written with steps easy to follow and replicate. The format for reporting a bug was properly followed. This made it really easy to post it on Jira. As expected, some of our defects were similar. For example both the pairs reported the atm dispensing the wrong amount when withdrawing cash. We worked together to split the faults that were common between the two reports so they both approximately have the same amount of faults. We also wrote the names of the member who found the fault in the report and assigned it to that specific member when reporting in Jira.

# How the pair testing was managed and team work/effort was divided 

Our team created a Whatsapp groupchat to communicate with one another. 

For the ET, we divided ourselves into pairs as follows:
Pair 1: Shahzill and Muteeba 
Pair 2: Rumaisa and Iman

One person in the pair ran the application on their device and performed tests according to their exploratory test plan, while the other person reported the defects as they were found.

For the MFT, we used the use cases in Appendix C: SUT Use Cases. We divided the 40 test cases equally amongst ourselves as follows:
- Use cases 1-10: Iman
- Use cases 11-20: Muteeba
- Use cases 21-30: Rumaisa
- Use cases 31-40: Shahzill

For the purpose of efficiency, if a certain member had finished performing their tests, they would start helping another member work through their use cases. This helped us save time during the MFT phase. 

When performing regression testing, we started by testing the defects already found in Version 1.0. Each individual tested Version 1.1 for the defects that they had found themselves in the previous. If the defect had been resolved, it was marked as “Done”. Otherwise, it was marked as “In Progress” and a comment was added stating “Defect still exists in Version 1.1”. In one case a defect had been resolved but not to the full extent. For example defect DL1-7, during the transferring of money instead of 10 dollars less being transferred, 10 cents less were transferred. In this case, we saw fit to mark the defect as “Done”, create a new one, and link it to this one with the “relates to” field. After rechecking our already found bugs, we went through all the use cases and tested them in Version 1.1 to ensure there were no new bugs that appeared. We followed the same procedure as the MFT, with each individual being assigned 10 use cases. 


# Difficulties encountered, challenges overcome, and lessons learned

It was all of our first time reporting defects in a bug tracking system. There was a bit of a learning curve in using the Jira application, but once we got the hang of it and figured out how to navigate our way around the system, it was very easy. We realised how useful the bug tracking system could be in the development of a large application as it can get very difficult to keep track of changes/defects. Moreover, being able to link issues to one another was also a feature we thought was very useful as the steps taken to resolve one issue could be replicated to solve a similar one.

Initially, we would realise we had found a bug but hadn’t kept track of the state of the system, or steps taken to replicate it. So we had trouble retracing our steps. As we got more familiar with tracking bugs, we ensured to be vigilant with which steps had been taken to reach a certain state in the system so we were aware of how to reach the bug.  


# Comments/feedback on the lab and lab document itself

Text…
