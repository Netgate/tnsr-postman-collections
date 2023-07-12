# TNSR Postman Collections

This public repo contains a Postman enviroment and Postman collection that can be used to interact with TNSR. TNSR is a high-performance software router based on FD.io's Vector Packet Processing (VPP). TNSR software combines VPP with Data Plane Developement Kit (DPDK) and other open-source technologies to provide a high-performace router which enables businesses and service providers to address today's edge and cloud networking needs.

You can edit the variables in the enviroment to point to your own TNSR device. Feel free to modify them as you see fit and add more calls to the collection.

## Setup

Setup TNSR before the Postman setup:
starting from TNSR release 23.06

```
{
    pki generate-restconf-certs length 4096
    restconf
        enable true
        global authentication-type user
        global server-certificate restconf
        global server-key restconf
        server host 0.0.0.0 443 true
    exit
}
```

TNSR also has cert-based authentication which is more secure and can be set up in Postman (out of scope of this document). For more details please refer to this [documentation](https://docs.netgate.com/tnsr/en/latest/recipes/restconf-pki-nacm/index.html). 

<hr/>

Follow these steps to setup Postman:

1. Download and install the desktop app at [Download Postman | Get Started for Free](https://www.postman.com/downloads/). Create a free Postman account to use the app.

2. Clone a [repository](https://gitlab.netgate.com/mukhamediev/tnsr-postman-collections/-/tree/main) and download TNSR collections.postman_collection.json and TNSR-enviroment.postman_environment.json files. 

3. 

