==================================
My Terraform Project for AWS EC2
==================================

This project sets up a t2.micro EC2 instance running Amazon Linux 2 in the us-west-2 region, with an SSH-accessible security group.

Pre-requisites
==============

- Terraform installed (https://www.terraform.io/downloads.html)
- AWS CLI installed and configured (https://aws.amazon.com/cli/)
- An SSH key pair available on the local machine

Clone the Repository
====================

Clone this repository to your local machine.

.. code-block:: bash

    git clone https://github.com/username/my_terraform_project.git
    cd my_terraform_project

Initialize Terraform
====================

Before you can apply your Terraform configuration, you need to initialize Terraform in your working directory.

.. code-block:: bash

    terraform init

Apply the Terraform Configuration
================================

After initialization, apply the Terraform configuration.

.. code-block:: bash

    terraform apply

When prompted, type "yes" to confirm that you want to create the resources. Terraform will then create the EC2 instance and related resources.

Access the EC2 Instance
=======================

Once the resources have been created, you can SSH into the EC2 instance using the private key that corresponds to the public key you specified in the Terraform configuration.

.. code-block:: bash

    ssh -i /path/to/your/private/key.pem ec2-user@<ec2-public-ip>
