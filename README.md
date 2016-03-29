This script does the following:

1. Provision a new AWS instance for the birt database if one does not exist.
2. Import all the bird data using the consume script.
3. Dump the database to an S3 bucket

# Usage:

Download the submodules:

```
git submodule init
git submodule update
```

Create a my_secure.yml file like this:

```
ec2_access_key: "your key here"
ec2_secret_key: "your key here"
```

Run this command:

```
sudo ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook site.yml --private-key grits-prod.pem
```

The instance needs to be terminated manually.
