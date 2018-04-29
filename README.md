Ansible Role: AWS VM Import Role
=========

Create the role and trust relationnship policy document used by AWS VM Import to import a virtual machine (VM) image from your virtualization environment to Amazon EC2 as Amazon Machine Images (AMI), which you can use to launch instances. 

Additional information can be found in the [AWS Documentation](https://aws.amazon.com/ec2/vm-import/).

Requirements
------------

None.

Role Variables
--------------

`s3_bucket_name`

The name of the S3 bucket where where the disk images to be convereted are stored. This is the only user provided variable required for the role.

`s3_bucket_arn`

The dynamically generated ARN of the S3 bucket provided in the `s3_bucket_name` variable and used in the `vmimport-policy.json.j2` template.

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: localhost
      gather_facts: false
      roles:
        - rubrik-devops.aws-vmimport-role
      vars:
        s3_bucket_name: "examplebucket-east-2"

License
-------

BSD

Author Information
------------------

<p></p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/8610203/37415009-6f9cf416-2778-11e8-8b56-052a8e41c3c8.png" alt="Rubrik Ranger Logo"/>
</p>
