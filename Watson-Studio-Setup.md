This tutorial walks you through setting up an account on the IBM Cloud and a project in Watson Studio such that you can use jupyter notebooks for your work.

# Configure Watson Studio

1. If you haven't been given a link to register already, please use the following link to create an IBM Cloud Account. It's completely for free, you don't need a credit card and the account never expires. => [http://ibm.biz/skillsnetwork](http://ibm.biz/skillsnetwork)
(Note: Please note that if you are using this link, your registration is tracked to skillsnetwork. This way you are indirectly supporting our courses.)

In case you are getting an error like below, please try with an different email address before you contact support. E.g. a non - gmail address..
![](https://github.com/IBM/coursera/raw/master/images/regfailure.png)

2. Once you've completed registration and confirmed your email address, please open [dataplatform.cloud.ibm.com](https://dataplatform.cloud.ibm.com) and click on "Log In"

![](https://github.com/IBM/coursera/raw/master/images/login.png)

3. Now please click on "Create a project"

![](https://github.com/IBM/coursera/raw/master/images/createproject.png)

4. Now please click on "Create an empty project"

![](https://github.com/IBM/coursera/raw/master/images/createemptyproject1.png)

5. Under "name", please type "default", then please click on "Add" under "Define Storage"

![](https://github.com/IBM/coursera/raw/master/images/addcos1.png)

6. Once you see the screen below, please scroll down

![](https://github.com/IBM/coursera/raw/master/images/addcos2.png)

7. Please make sure the "Lite" plan is selected, then please click on "Create"

![](https://github.com/IBM/coursera/raw/master/images/addcos3.png)

8. Please click on "Confirm"

![](https://github.com/IBM/coursera/raw/master/images/addcos3.png)

9. Please click on "Refresh"

![](https://github.com/IBM/coursera/raw/master/images/addcos5refresh.png)

10. Please click on "Create" to finalize project creation

![](https://github.com/IBM/coursera/raw/master/images/fincreateproject.png)

Congratulations, this concludes the first part of the tutorial. Please take a moment to follow through the next steps to learn how you can use Watson Studio jupyter notebooks.

# Create 1 CPU / 4 GB RAM environment
Watson Studio formerly included a free 1 CPU runtime. Unfortunately, this is not the case anymore. Fortunately, you get 50 capacity unit hours (CUH) for free usage every month and the smallest environment only consumes 0.5 per hours. This means you get 100 hours of free usage per month.

1. On the project page, please click on "Environments" and then on "New Environment Definition"

![](https://github.com/IBM/coursera/raw/master/images/addenv.png)

1. Please name it "supertiny" and make sure you've selected type "Default" with "1 vCPU and 4 GB RAM" with software version "Default Python 3.6"

![](https://github.com/IBM/coursera/raw/master/images/addenv2.png)

Congratulations, this concludes the second part of the tutorial. Please take a moment to follow through the next steps to learn how you can use Watson Studio jupyter notebooks.

# Using jupyter notebooks in Watson Studio

1. Please click on "Add to project"

![](https://github.com/IBM/coursera/raw/master/images/addtoproject.png)

2. Here you can select an abundance of tools, but let's go for jupyter notebooks first. Please click on "Notebook"

![](https://github.com/IBM/coursera/raw/master/images/addtoprojectnotebook.png)

3. In order to not use up only 0.5 CUH of your monthly 50 free CUH just select the "supertiny" runtime

![](https://github.com/IBM/coursera/raw/master/images/selectfreeruntime.png)

4. Please click on "Create notebook"

![](https://github.com/IBM/coursera/raw/master/images/createnotebook.png)

5. Just wait until the notebook appears. In case you are interested. The jupyter enterprise gateway has requested resources on the Kubernetes cluster IBM hosts for serving the jupyter kernel backing your notebook

![](https://github.com/IBM/coursera/raw/master/images/runtimerampup.png)

6. Now you're ready to code!

![](https://github.com/IBM/coursera/raw/master/images/testnotebook.png)


Congratulations, this concludes the third part of the tutorial. Please take a moment to follow through the next steps to learn how to stop an environment, just to make sure you are not consuming CUH in the background

# Stopping unused environments

1. From the project pages, please click on environments again

![](https://github.com/IBM/coursera/raw/master/images/listenv.png)

1. Under "Active environment runtimes" please click on the three dots and then on "Stop". Please make sure that all active runtimes have disappeared. 

![](https://github.com/IBM/coursera/raw/master/images/stopenvs.png)

This concludes this tutorial. 








