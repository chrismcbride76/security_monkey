Launch a GCP instance
=====================

Create an instance running Ubuntu 14.04 LTS using our 'securitymonkey' service account.

Navigate to the `Create Instance page`_. Fill in the following fields:

* **Name**: securitymonkey
* **Zone**: If using GCP Cloud SQL, select the same zone here.
* **Machine Type**: 1vCPU, 3.75GB (minimum; also known as n1-standard-1)
* **Boot Disk**: Ubuntu 14.04 LTS
* **Service Account**: securitymonkey

.. _`Create Instance page`: https://console.developers.google.com/compute/instancesAdd

Click the *Create* button to create the instance.

Install gcloud
^^^^^^^^^^^^^^

If you haven't already, install *gcloud* from the downloads_ page.  *gcloud* enables you to administer VMs, IAM policies, services and more from the command line.

.. _downloads: https://cloud.google.com/sdk/downloads

Connecting to your new instance:
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We will connect to the new instance over ssh with the gcloud command::

    $ gcloud compute ssh <USERNAME>@<PUBLIC_IP_ADDRESS> --zone us-west1-b

Replace the first parameter (<USERNAME>) with the username you authenticated gcloud with. Replace the last parameter (<PUBLIC_IP_ADDRESS>) with the Public IP of your instance.