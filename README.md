# Dark-Pattern-Analysis
This week, there are three tasks, all synthesis. For Task 1 and Task 2, we encourage that you write your code in Python 3 since we'll be able to provide the most detailed help if you do so. If you use Python, you can use a Jupyter Notebook, or you can just write your code in standard Python (.py) files. As usual, you'll be turning in both code and a PDF write-up.

Task 1: Synthesis: Missing Data (16 points)
Download the files, data.csv and data-full.csv. This dataset represents 18 years of music album reviews scraped from Pitchfork Links to an external site.and subsequently uploaded to Kaggle Links to an external site.. Specifically, we have taken the reviews table from that dataset and converted it to a CSV file.

You'll notice some missing data in four different columns in data.csv. Most of the missing data in the title and score columns was caused by us manually deleting data. The missing data in the author_type column was already missing in the dataset uploaded to Kaggle. There is also a small amount of data missing from the artist column, but you can ignore that.

You'll recall that we discussed patterns in missing data in Lecture 6. In this task, you will characterize this missing data, determining which pattern best appears to describe the missing data in the title, score, and author_type columns. Note that the pattern may or may not differ between these three columns with missing data.

(4 points) Without access to the full dataset, it is much harder to determine whether certain patterns apply. Thus, we've provided the full dataset as data-full.csv. You can cross-reference the values missing from data.csv by looking at data-full.csv. Based on this comparison, characterize the pattern governing the data missing from data.csv in the title and score columns.

Write-up Question 1 (4 points): In the write-up, present (and defend) your characterization of the missing data using the terminology (e.g., MCAR) introduced in lecture.

(4 points) Now pretend that you've never seen the full dataset. Characterize the data missing from the title, score, and author_type columns using the terminology introduced in lecture based only on the information contained in data.csv.

Write-up Question 2 (4 points): In the write-up, again present (and defend) your characterization of the missing data using the terminology introduced in lecture.

Task 2: Synthesis: Multiple Testing (28 points)
In this task, you will create a simulation to gain an intuition for type I errors (false positives) and type II errors (false negatives) in statistical hypothesis testing. This task assumes some basic knowledge of statistics. If you haven't seen basic statistics before, start with learning about the normal distribution Links to an external site., specifically the general normal distribution (where we specify a mean and a standard deviation). Then, read about the t-test or p-values in this tutorial Links to an external site.. You can also learn about Python's libraries for generating data following a normal distribution Links to an external site., running a t-test Links to an external site., and correcting p-values for multiple testing Links to an external site..

For these simulations, set alpha to be 0.05, which is fairly standard in computer science experiments involving human subjects. Use a two-sided t-test (testing that the distributions are different, rather than that one is larger than the other).

(3 points) First, create two normal distributions both with a mean of 8 and standard deviation of 2. Randomly sample n=30 points from each, and run a t-test to compare these two samples. Repeat this process automatically until you get a false positive (t-test result indicating that there is a significant difference between the two samples even though you know they came from the same distribution). Repeating this whole process until you are comfortable, about how many times on average do you need to run your simulation before getting a false positive?

Write-up Question 3 (2 points): In your write-up, report this average number of trials you determined.

(3 points) Now try varying n and graph the average number of trials required to get a false positive for different values of n.

Write-up Question 4 (2 points): In your write-up, include your graph and describe what you learned.

(1 point) Now repeat the previous simulation three times (including varying n) three times, using three different methods for correcting for multiple testing: Bonferroni, Holm, and Benjamini-Hochberg.

Write-up Question 5 (2 points): In your write-up, describe in prose how each of these three methods seems to impact type I errors (false positives).

(3 points) Now, create two normal distributions with means 7 and 9, respectively, and standard deviation 1.5 (for both). Note that, per the assumptions of the t-test, both distributions should have the same standard deviation, though the means should differ. Randomly sample n=30 points from each (again choosing n), and run a t-test to compare these two samples. Repeat this process automatically until you get a false negative (t-test result indicating that there is not a significant difference between the two samples even though you know they came from different distributions). Repeating this process until you are comfortable, about how many times on average do you need to run your simulation before getting a false negative?

Write-up Question 6 (2 points): In your write-up, report this average number of trials.

(3 points) Now try varying n, and graph the average number of trials required to get a false negative for different values of n.

Write-up Question 7 (2 points): In your write-up, include your graph and describe what you learned.

(2 points) Now repeat the previous simulation three times, using three different methods for correcting for multiple testing: Bonferroni, Holm, and Benjamini-Hochberg.

Write-up Question 8 (3 points): In your write-up, describe in prose how each of these three methods seems to impact type II errors (false negatives).

Task 3: Synthesis: Dark Patterns (56 points)
Recently, the New York Times ran an article about how the former president's re-election campaign used dark patterns Links to an external site.during last fall's campaign fundraising push. While the New York Times provides some screenshots, an article from Tech Dirt Links to an external site.provides even more screenshots and additional details.

In this part of the assignment, you will run your own empirical study to gauge the effect these dark patterns might have had. Test the specific types of dark patterns the campaign used, though you are free to switch the domain from politics into any other area.

Research Questions (0 points)
First, propose one or two precisely stated research questions about the dark patterns described in the articles linked above. Recall what we said about writing good research questions in class.

Interfaces (11 points)
Next, design and implement one or two pairs of interfaces (with experimental and control groups) to test the one or two research questions you described above. You can implement your interface in HTML, CSS, and/or JavaScript. If you haven't previously built a webpage, w3schools Links to an external site.has good tutorials for those languages. The most basic approach would probably be to create an HTML form with buttons Links to an external site.for the clickable parts of your page. If you would prefer, you could instead use an interface prototyping tool (InVision, Figma, etc.) that does not require any coding.

If you create the interface in HTML/JavaScript, you can host your page on https://people.cs.uchicago.edu/~YOURCNETID/. You can find instructions about how to do so from our department tech staff's help page. You could instead embed your interface within your survey (see below), though note that Qualtrics can zealously remove HTML and especially JavaScript (for good security reasons). You can also host it on any other site if you prefer.

Please include the files for your interface with your submission.

Survey (11 points)
You will (below) run an experiment where you test the impact of your dark patterns. Simply quantifying what people click on, though, only gives you partial insight into their experience. Design a short survey that supplements your quantitative measurements to better understand the specific dark patterns you are testing, and perhaps dark patterns more broadly.

Your survey should be short and to the point. As part of designing the survey, you should also provide appropriate instructions (e.g., explaining the task). Be sure not to bias your participants with the instructions you create. For the survey design, think carefully about what kind of data you are going to collect to answer your research questions. There is no restriction on what kind of questions you ask and what type of data you collect (quantitative or qualitative), but justify your choices in your final report.

For your survey implementation, we recommend using Qualtrics. To do so, please go to uchicago.qualtrics.com Links to an external site.and create an account with your UChicago account. To get familiar with Qualtrics, we think the following links might be helpful. You don't have to read all of them before starting, but they can be references when you need. If you would rather use Google Forms, Survey Monkey, etc., you are welcome to do so.

Survey basicsLinks to an external site.
Types of questions you can useLinks to an external site.
Display logicLinks to an external site.
Choice randomizationLinks to an external site.
Survey flowLinks to an external site.
Exporting dataLinks to an external site.
Query stringsLinks to an external site.
Note that the last of those links, about query strings, would be a good way to pass data (e.g., about which button the user clicked on) to your survey so that all of the information you need is in one place.

IMPORTANT: By the (annoying) terms of UChicago's Qualtrics site license, students are mostly not able to distribute a Qualtrics survey unless a faculty member creates the survey page. You can simply send a preview link Links to an external site.out, which looks much more janky but can be done even if Blase didn't create the survey.

Include your survey export as a PDF file ("Tools" --> "Import/Export" --> "Export Survey to Word" and then save it as a PDF) with the materials you submit.

Collecting Data (10 points)
Pilot the survey with five friends/family members/classmates. Think about components of cognitive interviews and think-aloud approaches that we discussed briefly in class that might help here.

The process by which you refine the design of your interfaces and survey should be iterative, which means you should design the survey, pilot it with one of your friends, update your survey or interfaces based on their feedback, and then pilot it with another friend.

You will submit the (anonymized!!!) data you collect as an xlsx, csv, or similar file.

Report (21 points)
Your report about this task, included as part of your write-up, must include the following parts:

Write-up Question 9: Research questions (4 points). Please specify what your research questions are. These research questions must be precisely stated, unambiguous, falsifiable, and concrete. Write-up Question 10: Interface Design (4 points). Please describe the design decisions you made in creating your interfaces and the reasons behind your design decisions. If you changed your design after piloting, please also include what suggestions your participants provided and what changes you made based on them. Write-up Question 11: Detailed Survey Design (4 points). Please briefly describe your survey protocol, such as what questions you have designed and what techniques you have used to make the survey more valid (and avoid confounds). For each question, please provide information such as why you put this question here, what types of data you hope to collect and how that can help you answer your research questions. If you thought about including other questions and chose not to include them, or eliminated them through piloting, include them here and explain why. Write-up Question 12: Piloting (4 points). Describe your process of running pilots and describe in detail what you changed about the interface and the survey after piloting, and why. Write-up Question 13: Analysis Plan (4 points). Please describe how you would analyze the data if you were to collect enough data in the future to make analysis meaningful. We acknowledge that your sample size is too small for analysis. Therefore, for this part, please imagine that you have already collected enough data for any analysis. What would you do to analyze them? Write-up Question 14: Results (4 points). Please provide and discuss your results. Because of the small sample size, you don't have to follow the analysis plan you proposed in the last part, but describe any interesting initial trends that could only be generalized with much more data. Your report will be graded based on the quality of your study design, not on the quality of your data. Therefore, don't worry too much if the data says your design doesn't work. Producing a valid and fair experiment and discussing your result objectively are what we value.
