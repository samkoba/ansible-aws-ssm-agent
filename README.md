# ansible-ssm-agent
 Script ansible for install ssm agent.

To install the Amazon SSM Agent on a Windows server using Ansible, you can use the win_package module. Here's an example playbook that installs the SSM Agent on a Windows host.

#Windows
This playbook will:

Check if the SSM Agent is already installed by checking the registry
If the SSM Agent is not installed, download the installer from Amazon's S3 bucket
Install the SSM Agent using the win_package module
You can customize the arguments passed to the win_package module to control the installation process. For example, you can pass the /quiet argument to install the agent silently.

You will need to have the win_reg_stat and win_get_url modules installed on your Ansible control machine. You can install these by running pip install ansible[windows].


##Linux
This playbook will:

Check if the SSM Agent is already installed by checking for the presence of the seelog.d/ssm-agent.cfg file
If the SSM Agent is not installed, install the dependencies required by the SSM Agent (Python 3, pip, and jq) using the package module
Download the SSM Agent installer from Amazon's S3 bucket
Install the SSM Agent using the package module
You can customize the arguments passed to the package module to control the installation process. For example, you can pass the -y argument to install the agent without prompting for confirmation.

I hope this helps! Let me know if you have any questions.