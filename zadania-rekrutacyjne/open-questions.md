Open questions

Please write answer to one (or more if you feel like) of the following open problems.

Note:

1. The answer should take about 100 to 500 words.

2. Feel free to google any information you might need.

3. Try to be concise, but precise.

4. The language matters. Use your long forgotten writing skills.

5. Please answer in English!

(2a) – Media protocols

Let's say we are hired to build a video trivia streaming mobile app, not unlike a very popular HQ Trivia app. It is your task to choose a video protocol best suited for this particular case. The issue is that we expect that the app will be used by up to 100 000 users solving quiz questions at the same time (and answering them within 10 seconds). Because of that, the chosen technology has to have low latency (less than 1 second) and cannot be very expensive in terms of CPU and network usage. What multimedia streaming protocols would you use for this problem and why? What are its strengths and weaknesses when comparing to others? How would you verify that the chosen protocols are a right choice for this case?

(2b) – Frontend performance

We are building a very complex Single Page App. The code base itself takes over 10 megabytes split over a thousand files and on top of that there are hundreds of images of varying sizes. Obviously, this is a problem, as we would like the app to load fast also on lower-end computers and mobile devices and on low network speeds. There are many methods to make this kind of app load fast – or that the user subjectively feels that it loads fast. Please choose a few you would like to apply here and describe them. What are the best ways to implement those methods? Or are there any good implementation already done?

(2c) – One app, different instances

Let's say we are developing an app for managing a software development agency that handles things like invoicing clients (through dedicated accounting software), workload planning, time tracking, client database (CRM) etc. etc. We intend to sell this app to about one hundred customers, i.e. other agencies. As each agency has slightly different needs, we would like to be able to customize the code of each instance. In particular, some agencies might have a different accounting software to integrate with, or some would like to use only some of the modules, or there might be a slightly different business logic for particular feature for each agency, or some might want to customize the look and feel of the app – or ultimately, some of the agencies would like to have custom features developed for them (and are of course ready to pay for that). Propose a solution that will allow us to have 100 slightly different versions of the same app. We will need to maintain all the instances, so it is important that it is quite easy. In particular, if we fix a bug for one instance, we would like to easily propagate the bugfix to all the other instances. If we create a custom feature for one customer, we would like to easily add it to other instances if the other customers also want to have it. Of course there is no single best method to handle all the maintenance issues, so choose one or two that you like and describe it. What advantages and disadvantages does it have? Are there any cases for which this particular method is better than others?
