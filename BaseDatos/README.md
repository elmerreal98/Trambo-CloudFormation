
# BaseDatos/bd.yml
The file [bd](/BaseDatos/bd.yml) is the template that allows create a RDS instance:

The strcuture of the file is the following:

* Description

* Parameters
    * RefSubnetsPrivadas
        * String separate by commas of the private subnets
    * RefSG
        * Security group that just have port 3306 open.
    * RefDefaultSG
        * Security group default of the VPC.

* Resources
    * SubnetGroup
        * Creates a subnet group with the ids of all the subnets received as parameter.
    * MyDB
        * Creates a RDS instance.

* Outputs
    * EndpointBD
        * Returns the endpoint of the instance