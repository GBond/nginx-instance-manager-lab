Introduction
============

The purpose of this Lab is to introduce NGINX Instance Manager. NGINX 
Instance Manager is designed to make NGINX even easier to configure,
use and maintain.  We designed it from the ground up to be in line with
the experience you expect from NGINX (small, lightweight, fast).  NGINX
Instance Manager is our latest product offerring and the lab is designed
to showcase how to get started with it and what it can do.

NGINX Instance Manager is focused on using existing NGINX instances and 
the concepts in this lab can be applied to production environments.

Background
==========

`NGINX <https://nginx.org/en>`__ and `NGINX 
Plus <https://www.nginx.com/products/nginx>`__ itself uses a native 
configuration lanugage ("NCL") that leverages the linux flat file 
and directory structure.  A main `nginx.conf` file will have 
multiple includes that typically will be in directories.  This allows 
shared configurations and isolation for individual instances. NGINX 
can also be deployed on many different form factors and integrates 
well into CI/CD pipelines.

NGINX has become a very popular application and is the most used web server 
on the internet today.  NGINX Instance Manager extends the existing 
functionality of NGINX by adding an API, metrics and Analyzer functionality. 
It is a native NGINX management solution.


Overview
========

This Lab guide will help you complete the following:

1. Install, enable and configure NGINX Instance Manager using native linux tools.

2. Utilize the scanner function in NGINX Instance Manager to discover new instances.

3. Deploy the nginx-agent to existing NGINX instances.

4. Manage configurations of NGINX instances and utilize NGINX Analyzer for suggestions.

5. Display the metrics of NGINX instances.

6. Explore the API of NGINX Instance Manager.

Lab Goals
=========

During this lab you will make use of NGINX Instance Manager 
to discover, manage and produce metrics for NGINX Open Source 
and NGINX Plus instances.

Getting Started
---------------

The infrastructure is already setup for you; however, we are going to clear 
out everything so we can practice the installation steps.  To do this, we 
will utilize ssh to connect to the nginx-manager server and run the 
`reset.sh` script in the home directory of the centos user.

The **nginx-manager** is the instance that provides the NGINX Instance Manager 
API, metrics endpoint and user interface to use.  It also functions as the 
reciever for the nginx-agent component on the NGINX instances.
**Run all lab activities from the nginx-manager unless specified**

Lab Topology and Credentials
----------------------------

The NGINX machines are there to provide a cross section of installation 
options.

NGINX Instances:

+--------------+----------------------+--------------+-------------+
| **Instance** | **FQDN**             | **OS**       | **NGINX**   |
+--------------+----------------------+--------------+-------------+
| OSS-Centos   | nginx5.f5demolab.com | Centos 7     | Open Source |
+--------------+----------------------+--------------+-------------+
| OSS-Ubuntu   | nginx6.f5demolab.com | Ubuntu 18.04 | Open Source |
+--------------+----------------------+--------------+-------------+
| Plus-Ubuntu  | nginx7.f5demolab.com | Ubuntu 18.04 | Plus        |
+--------------+----------------------+--------------+-------------+
| Plus-Centos  | nginx8.f5demolab.com | Centos 7     | Plus        |
+--------------+----------------------+--------------+-------------+

Expected time to complete: **1 hour, 30 minutes**

*A listing of the modules for this class is listed below.  This same list is also available on the left column of every page for direct access.*

.. toctree::
   :maxdepth: 1
   :caption: Content:
   :glob:

   intro
   module*/module*