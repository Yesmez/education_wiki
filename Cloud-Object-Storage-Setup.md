In order to store and retrieve data from notebooks it is important to properly setup IBM Cloud Object Storage (COS). COS is S3 compatible and represents the most cost effective way of persisting large data sets.

Although, in the context of a single notebook execution a transient filesystem is available, it is not possible to store data beyond the life cycle of an individual notebook. Also sharing data between notebooks is not possible.

In the IBM Lite plan for cloud object storage 5 GB of data can be stored for free. In case more is needed, simply switch the storage plan so an infinitely large storage pool becomes available and only data stored is charged.

To find out more about the pricing, please visit the [pricing overview](https://www.ibm.com/cloud/object-storage/pricing?cm_mmc=Email_Events-_-Developer_Innovation-_-WW_WW-_-romeo-kienzler\CourseraCouraseAppliedAIusingDeepLearning\unknown\unknown\unknown\unknown\online\unknown&cm_mmca1=000019RS&cm_mmca2=10004805&cm_mmca3=M99938765&cvosrc=email.Events.M99938765&cvo_campaign=000019RS).

You can create a standard plan Cloud Object Storage Service [here](https://cloud.ibm.com/catalog/services/cloud-object-storage?cm_mmc=Email_Events-_-Developer_Innovation-_-WW_WW-_-romeo-kienzler\CourseraCouraseAppliedAIusingDeepLearning\unknown\unknown\unknown\unknown\online\unknown&cm_mmca1=000019RS&cm_mmca2=10004805&cm_mmca3=M99938765&cvosrc=email.Events.M99938765&cvo_campaign=000019RS)

If you are fine with the 5 GB storage limitation just work with the free COS.

1. To access it, in IBM Cloud Pak for Data, on the project page, please click on settings:

![](https://github.com/IBM/coursera/raw/master/images/cos2nb1.png)

2. Then please click on Storage->"Manage in IBM Cloud"

![](https://github.com/IBM/coursera/raw/master/images/cos2nb2.png)

3. Click on "Create Bucket"

![](https://github.com/IBM/coursera/raw/master/images/cos2nb3.png)

4. Click on "Quick start"

![](https://github.com/IBM/coursera/raw/master/images/cos2nb4.png)

4. Click on "Next" and note down the auto-generated bucket name and assignt it to the "bucket_name" in the notebook

5. Then again, click on "Next", then click on "View Bucket configuration". Please note down the public endpoint and assign it to the "endpoint" variable in the notebook

![](https://github.com/IBM/coursera/raw/master/images/cos2nb6.png)

6. Click on "Service Credentials"

![](https://github.com/IBM/coursera/raw/master/images/cos2nb7.png)

7. Click on "New Credential". Leave the default, but please enable under advanced options,  "Include HMAC Credential". Then click on add

![](https://github.com/IBM/coursera/raw/master/images/cos2nb8.png)

8. Expand on the newly created service credential and copy-paste the entire contents

![](https://github.com/IBM/coursera/raw/master/images/cos2nb9.png)

9. Paste the contents of the credentials to the notebook, please make sure that the final result looks similar to the following screen shot (e.g. that also endpoint and bucket_name has been set)

![](https://github.com/IBM/coursera/raw/master/images/cos2nb10.png)