---
layout: default
title:  "{{ site.name }} - UNICORE @ PLGrid"
---

## PLGrid (and ICM) Production UNICORE Infrastructure

Please see [PLGrid manual](http://docs.plgrid.pl/unicore) about UNICORE (in polish).

ICM users may also see [ICM user manual](https://www.icm.edu.pl/kdm/Podr%C4%99cznik_u%C5%BCytkownika) (also in polish).

## Testbed UNICORE Infrastructure

W skład sajtu testowego wchodzą następujące usługi:
*  Registry
*  2 instancje Unicore/X oraz 2 instancje TSI
*  Workflow i Servorch
*  Unity IDM
*  Accounting
zapewniające dostęp do dwóch "wirtualnych" ośrodków obliczeniowych: PLG-ICM-TEST oraz PLG-NCU-TEST.

Usługi sajtu zainstalowane są na 4 serwerach:

*  testbed.nebula.grid.icm.edu.pl: Gateway, Registry, Workflow, Servorch
*  testbed.grid.icm.edu.pl: Gateway, Unity, Unicore/X, TSI
*  unicore.studmat.umk.pl: Gateway, Unicore/X, TSI
*  alces.grid.icm.edu.pl: Acconting

Na każdym serwerze jest ponadto zainstalowana lokalna baza danych (MySQL), wykorzystywana przez działace na nim usługi.

Główny rejestr dostępny jest pod adresem:

https://testbed.nebula.grid.icm.edu.pl:8080/TESTBED/services/Registry?res=default_registry

Rejestry lokalne PLG-ICM-TEST i PLG-NCU-TEST dostępne są natomiast odpowienio pod adresami:

https://testbed.grid.icm.edu.pl:8080/PLG-ICM-TEST/services/Registry?res=default_registry

oraz

https://unicore.studmat.umk.pl:8080/PLG-NCU-TEST/services/Registry?res=default_registry

Zadania zlecane w ośrodku PLG-NCU-TEST wykonywane są na lokalnym dwuwęzłowym klastrze zbudowanym w oparciu o wirtualizację (system kolejkowy Torque), natomiast zlecane w ośrodku PLG-ICM-TEST - na klastrze HYDRA w ICM (system kolejkowey SLURM).

Uwierzytelnianie oparte jest w całości o testową instancję Unity - nie są wykorzystywane inne instancje Unity lub UVOS. Zlecanie zadań testowych jest możliwe dla użytkowników posiadających konto w ldapie ICM lub dodanych lokalnie do bazy Unity (dla użytkowników nie posiadających konta w ldapie). Usługi nie są dostępne dla użytkowników posiadających jedynie konto w ldapie PL-Grid. Niezbędne jest również posiadanie certyfikatu osobistego, zgodnego z wymaganiami PL-Grid. Formularz logowania do Unity dostępny jest pod adresem:

https://testbed.grid.icm.edu.pl:2443/user/home

natomiast panel admina:

https://testbed.grid.icm.edu.pl:2443/idm/admin
