# centos7_chefnode - testing docker hub autobuild 
A docker image to run containers as Chef nodes.



The containers created with this image will have ssh access for bootstraping Chef nodes.

To create a container:
`docker run -d -P --name mychefnode douglax/centos7_chefnode`

Check the port 22 is mapped to:
`docker port mychefnode`

Check ip address of the node:
`docker inspect mychefnode`

Connect to the container via ssh:

`ssh kitchen@<container_ip_address>`
or
`ssh kitchen@<host_ip_address> -p <mapped_port>`

password is _kitchen_ 
root password is _kitchenroot_
