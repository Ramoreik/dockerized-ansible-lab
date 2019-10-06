# Ansible Dockerized Lab

This playbook and set of roles is used in order to create containers in a configuration based way.



There are four variables files in the "constants" folder:

1.  Images : Contains the configuration for images to build from dockerfiles or to pull from a given docker registry.

2.  Volumes : Contains the configuration for the volumes needed for diverse container setups.

3.  Networks : Contains the configuration for the networks needed in your service.

4. Lastly Containers: This containers the configuration to link the images, volumes and network to a container.

The playbook called "deploy_environment.yml"  will orchestrate the creation of the images, volumes, networks and container.



This playbook has 2 options for now but will most likely have more:

1.  desired_state: This will take over the default for the state of containers. (default being present)



2. force_rebuild: This will force the rebuild of images, usefull if one of the layers in your image needs to change and docker doesn't deem the change big enough.



This will allow you to deploy pretty much any service for testing purposes within your own dev environment.
