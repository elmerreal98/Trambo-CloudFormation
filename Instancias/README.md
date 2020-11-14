# Instancias/wordpress.yml
In the file [wordpress](/Instancias/wordpress.yml) is the template that allows create EC2 instances.

The strcuture of the file is the following:

* Description

* Parameters
    * RefSubnetPublica
        * String of the public subnet id
    * RefSG
        * Security group that just have port 80 and 22 open.
    * RefDefaultSG
        * Security group default of the VPC.
    * EndpointBD
        * Endpoint of RDS created

* Resources
    * MyEC2Instance
        * EC2 instance with wordpress installed via user data.
