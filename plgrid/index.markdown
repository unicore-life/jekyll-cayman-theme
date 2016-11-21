---
layout: default
title:  "{{ site.name }} - UNICORE @ PLGrid"
---

## PLGrid (and ICM) Production UNICORE Infrastructure

Please see [PLGrid manual](http://docs.plgrid.pl/unicore) about UNICORE (in polish).

ICM users may also see [ICM user manual](https://www.icm.edu.pl/kdm/Podr%C4%99cznik_u%C5%BCytkownika) (also in polish).

## Testbed UNICORE Infrastructure

There are following services in the test site:
*  Registry
*  two instaces of Unicore/X or two instances of TSI
*  Workflow i Servorch
*  Unity IDM
*  Accounting

Services allows access to two virtual sites: PLG-ICM-TEST and PLG-NCU-TEST.

Services of the test site are installed on following four servers:

* **testbed.nebula.grid.icm.edu.pl**: Gateway, Registry, Workflow, Servorch
* **testbed.grid.icm.edu.pl**: Gateway, Unity, Unicore/X, TSI
* **unicore.studmat.umk.pl**: Gateway, Unicore/X, TSI
* **alces.grid.icm.edu.pl**: Acconting

On each server there is local data base (mysql), which is used by installed services.


The main register is available on:

    https://testbed.nebula.grid.icm.edu.pl:8080/TESTBED/services/Registry?res=default_registry

Local registres PLG-ICM-TEST and PLG-NCU-TEST are available on:

    https://testbed.grid.icm.edu.pl:8080/PLG-ICM-TEST/services/Registry?res=default_registry

and

    https://unicore.studmat.umk.pl:8080/PLG-NCU-TEST/services/Registry?res=default_registry

Jobs placed in PLG-NCU-TEST site are executed on local two-node cluster based on virtualization (queque system - Torque) and jobs placed in PLG-ICM-TEST site are executed on HYDRA cluster in ICM (queque system - SLURM).
	
The authorization is based on test instance of Unity - other istances of Unity and UVOS are not used.
Executing jobs on the test site are allowed only for users who have account in the ICM ldap or who are added to the local Unity database (for users who haven't an ldap account). Services are not available for users who have account only in the PL-Grid account. All users must have a personal certificate, which is validated by PL-Grid.
Login form is available on:
	

    https://testbed.grid.icm.edu.pl:2443/icm/home

The admin planel:

    https://testbed.grid.icm.edu.pl:2443/idm/admin
    
To authenticate in UCC or URC client you have to use the following link:

    https://testbed.grid.icm.edu.pl:2443/testbed/saml2unicoreidp-soap/AuthenticationService
