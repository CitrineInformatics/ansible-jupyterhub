This role installs Jupyter, JupyterHub and sudospawner using Python 3.
 
It has been tested with Ubuntu 16.04 and works as of 07-2017.

JupyterHub is installed as per instructions, with node.js and configurable-http-proxy.

#### To run:

  -  Install Ansible
  -  Add an IP address to the hosts file, under `[jupyterhub]` 
  -  Run the following command:

    ansible-playbook no_ssl.yml -i hosts -u ubuntu

When everything has finished you should be able to point your browser at:

    http://<ip address>:8000

And then login as jupyter with the password you entered at the start.

To add a user, login to the server as root:

    adduser <username>
    addgroup <username> jupyter

Then connect via web browser

    http://<ip address>:8000
