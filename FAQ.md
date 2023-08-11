# How to get started?
Please make sure to follow the tutorial to the tack, otherwise you might run into errors: https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup

# Why is the setup of the learning environment so complicated?

Using a complex cloud environment is complicated. Initially, we thought that learners this way get a real feeling how Data Science projects in the Cloud look like. But we've received quite a few complaints, therefore we have removed all requirements for generating data and provide all notebooks to point to a data source with pre-poulated data

# Where do I get Apache Spark from?

Spark is installed for you automatically inside the notebook, so there is no need to use the environment provided by Watson Studio


# How do I share a GIST of my notebook

First of all, you don't need to share a GIST, you can also use the built-in share functionality in Watson Studio. 

- Just make sure you got to File->Save Version first. 
- Then click in the share icon and select the "All content, including code" checkbox. 
- Then share the link displayed, but please be aware that always the latest saved version of the notebook is shared, so in case you want to share changes please save a new version. 

Alternatively, you can share a GIST. 

- In IBM Watson Studio (dataplatform.cloud.ibm.com) open the notebook causing trouble
- Then click on File->Download as->Notebook (.ipynb)
- Then open this file in a text editor. Open https://gist.github.com/
- Paste the contents into the text area
- Finally assign a name ending with .ipynb and click on "create secret gist".

Then share the link to the GIST in the forum


# Account activation email ends up in spam filter
I am trying to create an account on the IBM Cloud and when it sends out an email to confirm the account I don't get it. I assume my spam filter is filtering out. For those of you who have not deleted the confirmation email could you tell me the address it came from so I can enter that into the allowed list on the filter.

=> no-reply@cloud.ibm.com


# The peer review takes a long time, my subscription is about the expire

On a regularly basis (e.g. every week or so) I'm assessing the last submissions which didn't get 3 reviews within the last 2 weeks. In case this takes to long for you (e.g. subscription expires) please ping us in the forum. Worst case please file a ticket with coursera afterwards and let us know the ticket number so we can support the case with coursera

# Usage Limit Reached (of Watson Studio Runtime)

Watson Studio formerly included a free 1 CPU runtime. Unfortunately, this is not the case anymore. Fortunately, you get 50 capacity unit hours (CUH) for free usage every month and the smallest environment only consumes 0.5 per hours. This means you get 100 hours of free usage per month. Please make sure you've followed the [tutorial](https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup), especially the [part](https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup#create-1-cpu--4-gb-ram-environment) which tells you how to [create](https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup#create-1-cpu--4-gb-ram-environment) and [use](https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup#using-jupyter-notebooks-in-watson-studio) the "supertiny" environment. Please use this one exclusively. In case Apache Spark is needed, the notebooks are installing Spark for you. So no need for using the Watson Studio provided Apache Spark environments. In case you have used up your CUH's for this month there are the following options:

1. Upgrade your IBM Cloud account (requires a Credit Card), but you get US$200 for free which you can use. But take care of your consumption then as anything exeeding US$200 will be debited to your card
1. Wait until the period ends and your CUH renew
1. Create a new IBM Cloud Account on ibm.biz/skillsnetwork using a different email id (https://temp-mail.org is your friend :)


# if there is anomaly in the data the reconstruction error will show that in that place something is wrong. But if the neural network sees it once and next time that shape/point appears, it will be treated as normal data. How can this thing can be overcome ?

the way to do it is using semi-supervised learning

1st, you need to add continuous check-pointing of your weights

then on an alert a domain expert needs to verify if it was a true alert, if yes, rollback training to the weights on the checkpoint before the alert was triggered, otherwise just continue, next time likelihood of a false positive is less

note: this system works only for stationary data


# syntax error, lambda notation python 2.7 vs 3.x

`result_array_ts = result_rdd.map(lambda (ts,voltage): ts).collect()`
SyntaxError: invalid syntax 

Please use either python 2.7 or change the syntax to:

`result_array_ts = result_rdd.map(lambda ts_voltage: ts_voltage[0]).collect()`

`result_array_voltage = result_rdd.map(lambda ts_voltage: ts_voltage[1]).collect()`

#I am just starting it today. But it says I have to submit the first week assignment in 1 min. When does then next schedule start?

You can join and switch sessions and taking you credit over the sessions so no need to worry




# how do i stop the kernel, and how to make sure it is not running?

got to the assets tab of your project (closing the notebook first)

in the notebooks table find your notebook

find the 3 vertical dots on the left hand side and open the menu by clicking on it

in case you see a lock, first unlock the notebook then you will get the stop kernel option.

select stop kernel (hint: sometimes you need to wait for 2-3 seconds until the option appears)



# 'JavaPackage' object is not callable
Systemml is not installed properly, please follow the instructions to the tack provided in the notebook

# I have a problem with the user interface from Coursera, e.g. buttons not working etc..
please try:
* reboot
* delete cookies
* use other browser
* use other computer
* start over using a different email id 

if problem persists, please open a ticket with coursera https://www.coursera.org/about/contact - in case you can't find a way to contact them please use https://learner.coursera.help/hc/en-us/articles/360024928831-Chat-with-us and the chat box bottom right

# Usage limit reached
Please have a look at [this](https://github.com/IBM/skillsnetwork/wiki/FAQ#usage-limit-reached-of-watson-studio-runtime) entry

# invalid Email Or Token
Please make sure you only change email and token variables and not the key variable. Please make sure you obtain the token from the coursera's grader page

# how do I post assignments to the grader?
I've created a video for you explaining this :)
https://www.youtube.com/watch?v=GcDo0Rwe06U

# I don't have option for adding a notebook in IBM Watson Studio
1. open dataplatform.cloud.ibm.com
1. Please click on the circle icon top right corner
1. Click on "Profile and Settings"
1. Click on the "Apps" tab
1. Please verify that you have a (free, never expiring) Watson Studio subscription (by choosing the "Lite" plan)

# Failed to Start the Kernel
you have to hover over the "not trusted field" and select "trust" in order to successfully run the notebook

# I already have an existing IBM Cloud account, do I need to create a new one?
please go ahead and use the existing one, one thing, IBM changed from a trial model to a freemium model, this means, your account now doesn't expire anymore, if this is the case with your old one, please go ahead and use the old one, in case your old account expire(s)(d), just create a new one using a different email id =>

http://ibm.biz/coursera

If you use the link above, it counts towards Coursera and helps to support our courses :)

# Why are we still teaching DeepLearning4J and SystemML in this course?
By the time we've created the course the deep learning framework landscape was much more hybrid. Nowadays mainly TensorFlow/Keras and PyTorch are used. Therefore, we are removing DeepLearning4J and SystemML in the next version of this course. This means scaline DeepLearning on Apache Spark is getting a bit harder. We've had some fun with Elephas, so you can have a look. It runs Keras on Spark: https://github.com/IBM/coursera/blob/master/coursera_ai/week4/elephas_example.ipynb. Most clusters are training Deep Learning using Horovod or TensorFlow Parallel Training though. 

# I have completed all 4 coursed of the the Advanced Data Science Specialization and received individual badges for each course. But I have not received the specialization badge yet. 

This can take up to one month. If it takes longer, please let us know...

# I don't see an option to add a notebook
1st, please make sure you've created a project in Watson Studio on dataplatform.cloud.ibm.com. Then, sometimes this happens. Please go to your initials top right, then on "profiles and settings", then on "Apps". Then please add the "Watson Studio" in the "lite" plan

# I'm feeling lost and confused, please help me!
We fully understand that we expect a lot and that we throw a lot of information at you. We often get questions like: "I'm feeling lost and confused, please help me!" - This actually doesn't help. We need to know WHERE EXACTLY you feel lost and confused. So please tell us in which video or exercise. In case you have a problem with a notebook, please share it => https://github.com/IBM/skillsnetwork/wiki/FAQ#how-do-i-share-a-gist-of-my-notebook Please also include screenshots if necessary...  

# No module named 'rklib'
please execute all cells top to bottom in the correct order. In case you are not using Watson Studio please either install the "wget" command or download rklib manually

# Why do you only support IBM Watson Studio during the course
First of all, because this course is created by IBM - so of course some of the IBM folks really want to show our cool cloud product. This is fine since you don't need a credit card and the account never expires and everything is for free for 100 hours per month and running on open source. But a side note on a more practical side. We've tried to teach this course (online and offline) with learners using their local environments and we ended up in spending 80% of the time in trying to fix those local installations. So I hope you understand that in the forums we can only support Watson Studio. But please be assured: All the code CAN be made running on ANY jupyter environment, either in the cloud or locally, we just don't have the bandwidth to support you there, thanks a lot for your understanding. This should NOT STOP you to use a different environment, it is up to you and it might work as well.

# unsupported operand type(s) for +: 'range' and 'list'
You might have copied code by typing it from what you have seen in a video. In python 3.x you need to explicitly cast a range to list by: list(range(n)). The templates are all updated, but not the videos, sorry for the inconvenience

# how to handle missing values?

* delete (rows containing at least one missing value in at least one column you need)
* set to zero
* impute (by considering nearby data points)


# name 'sc' is not defined / name 'spark' is not defined
As we are running in the free, non-spark notebooks, a spark test environment needs to be installed. This is done in all the templates you can find in GitHub. In case you start coding from scratch, please run the first four code cells of this notebook first: https://github.com/IBM/skillsnetwork/blob/master/coursera_bd/week4/a6_w4_assignment.ipynb

# Where can we get notebook files used in all the videos?
We've unfortunately lost some of them, so sorry. All we have is on https://github.com/IBM/skillsnetwork. Each course has it's own folder

# Your account cannot be created at this time. Code: XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
We are currently investigating. It seems that some email addresses aren't working. Worst case, try to use https://temp-mail.org - as of now it works....

# AssignementML4 / AssignmentSystemML: Permission denied when trying to make directory
Please make sure that you are running inside a "normal" runtime and NOT in a Apache Spark runtime from Watson Studio => https://github.com/IBM/skillsnetwork/wiki/Watson-Studio-Setup

# TypeError: can only concatenate list (not "range") to list
Please use : [101] + list(range(100))

# I'm an IBMer, do I have to pay for the courses?
yes. but you can take it in audit mode. just click on enroll and then there is a small link for audit mode (despite the big button) - so watch out for it. In 2023 there is a promotion for IBMers: https://www.coursera.org/promo/IBMemployee