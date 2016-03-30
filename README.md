Otto workshop
=============

Compile
-------

`$ otto compile`

Samler inn informasjon om applikasjonen i $PWD og lagrer informasjonen i `.otto/`

Auto-detekterer flere typer applikasjoner.

- Nodejs
- PHP
- Go
- Ruby
- Python
- Java (ganske så beta)
- Docker

Status
------

`$ otto status`

Viser informasjon om prosjektet, samt tilstanden til de ulike trinnene.

Dev
---

`$ otto dev`

Bygger en virtuell maskin via Vagrant og installerer runtime avhengigheter basert på applikasjonstype.

Logg inn på maskinen med

`$ otto dev ssh`

Infra
-----

`$ otto infra`

Bygger en best-practice infrastruktur med Terraform. Enn så lenge er AWS den eneste infrastruktur typen.

AWS Infra typen kommer i to varianter.

- simple: VPC med public subnet, enkelt Consul oppsett
- vpc-public-private: VPC med ett public og ett private subnet, NAT instans, Bastion host i public subnet, Consul cluster

Build
-----

`$ otto build`

Bygger et egnet binary image for skyplattformet ved hjelp av Packer.

Deploy
------

`$ otto deploy` 

Deployer AMI til infrastrukturen.

Avslutte
--------

`$ otto deploy destroy`

`$ otto infra destroy`

`$ otto dev destroy`

River ned igjen alle ressurser som har blitt opprettet av Otto.

