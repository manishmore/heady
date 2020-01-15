# Install Ansible.
First of all, you should install Ansible on your local computer.

# Modify:
Modify /hosts file:
You should add your AWS access key and AWS secret key:

# Run Ansible playbook
$ ansible-playbook -b aws_monitoring_playbook.yaml

# Manually test monitoring scripts.

Go to CloudWatch -> Metrics ->Linux System ->Instanceld. There are metrics for utilization of RAM
Information of disk space is CloudWatch -> Metrics ->Linux System -> Filesystem, InstanceId, MountPath
