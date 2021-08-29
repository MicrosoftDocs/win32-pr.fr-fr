---
description: Les interfaces de programmation utilisées pour interroger les différents types d’espaces de noms et pour enregistrer des informations dans un espace de noms, si elles sont prises en charge, diffèrent considérablement.
ms.assetid: 6a037e8d-49f3-4286-929a-8bb64ea0960f
title: Architecture du fournisseur d’espace de noms dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2f29b0bb5d432639fddff94430e76970e14f8bbbfe91f8b8478f2ee804c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758029"
---
# <a name="namespace-provider-architecture-in-the-spi"></a>Architecture du fournisseur d’espace de noms dans le SPI

Les interfaces de programmation utilisées pour interroger les différents types d’espaces de noms et pour enregistrer des informations dans un espace de noms, si elles sont prises en charge, diffèrent considérablement. un fournisseur d’espaces de noms est une application résidente localement qui peut être mappée entre l’index SPI de l’espace de noms Windows sockets et un espace de noms existant qui peut être implémenté localement ou accessible via le réseau. Cette procédure est illustrée comme suit :

![diagramme du fournisseur d’espaces de noms](images/ovrvw3-1.png)

> [!Note]  
> Il est possible pour un espace de noms donné, par exemple DNS, d’avoir plusieurs fournisseurs d’espaces de noms installés sur un ordinateur donné.

 

Comme indiqué ci-dessus, le terme générique, service, fait référence à la moitié du serveur d’une application client/serveur. dans Windows sockets, un service est associé à une classe de service et chaque instance d’un service particulier a un nom de service qui doit être unique dans la classe de service. le serveur FTP, SQL Server, XYZ Corp. employee Info server, etc. sont des exemples de classes de service.

Comme l’exemple tente d’illustrer, certaines classes de service sont bien connues, tandis que d’autres sont uniques et spécifiques à une application verticale particulière. Dans les deux cas, chaque classe de service est représentée par un nom de classe et un identificateur de classe. Le nom de classe ne doit pas nécessairement être unique, mais l’identificateur de classe doit être. Les identificateurs globaux uniques (GUID) sont utilisés pour représenter des ID de classe de service. Pour les services connus, les noms de classe et les identificateurs de classe (GUID) ont été préalloués, et les macros sont disponibles pour la conversion entre, par exemple, les numéros de port TCP et les GUID d’identificateur de classe correspondants. Pour les autres services, le développeur choisit le nom de la classe et utilise l’utilitaire Uuidgen.exe pour générer un GUID pour l’identificateur de classe.

Le concept d’une classe de service existe pour permettre l’établissement d’un ensemble d’attributs qui sont communs à toutes les instances d’un service particulier. cet ensemble d’attributs est fourni à Windows sockets au moment où la classe de service est définie et est appelé informations de schéma de la classe de service. Le \_32.dll Ws2 relaie ensuite ces informations à tous les fournisseurs d’espaces de noms actifs. Quand une instance d’un service est installée et mise à disposition sur un ordinateur hôte, son nom de service est utilisé pour distinguer cette instance particulière des autres qui peuvent être connues de l’espace de noms.

N’oubliez pas que l’installation d’une classe de service ne doit se produire que sur les ordinateurs sur lesquels le service s’exécute, et non sur tous les clients qui peuvent utiliser le service. Lorsque cela est possible, le \_32.dll Ws2 fournit des informations de schéma de classe de service à un fournisseur d’espace de noms au moment où une instance d’un service doit être inscrite ou qu’une requête de service est lancée. Le \_32.dll Ws2 ne stocke pas ces informations elles-mêmes, mais tente de les récupérer à partir d’un fournisseur d’espace de noms qui a indiqué sa capacité à fournir ces données. Étant donné qu’il n’y a aucune garantie que la32.dll Ws2 pourra \_ fournir le schéma de la classe de service, les fournisseurs d’espaces de noms qui nécessitent ces informations doivent disposer d’un mécanisme de secours pour l’obtenir via des moyens spécifiques à l’espace de noms.

Le système de noms de domaine Internet ne dispose pas d’un moyen bien défini pour stocker les informations de schéma de la classe de service. Par conséquent, les fournisseurs d’espaces de noms DNS peuvent uniquement prendre en charge les services TCP/IP connus pour lesquels un GUID de classe de service a été préalloué. Dans la pratique, il ne s’agit pas d’une limitation sérieuse dans la mesure où les GUID de classe de service ont été préalloués pour l’ensemble des ports TCP et UDP, et les macros sont disponibles pour récupérer le GUID associé à n’importe quel port TCP ou UDP. Ainsi, tous les services familiers, tels que FTP, Telnet, Whois, etc., sont bien pris en charge. Lors de l’interrogation de ces services, le nom d’hôte de l’ordinateur cible est, par Convention, le nom de l’instance de service.

En poursuivant notre exemple de classe de service, les noms d’instance du service FTP peuvent être « alder.intel.com » ou « rhino.microsoft.com », tandis qu’une instance du serveur d’informations d’employé XYZ peut être nommée « XYZ Corp. Employee info Server version 3,5 ». Dans les deux premiers cas, la combinaison du GUID de la classe de service pour FTP et du nom de l’ordinateur (fourni comme nom de l’instance de service) identifie de manière unique le service souhaité. Dans le troisième cas, le nom d’hôte où se trouve le service peut être découvert au moment de la requête de service, de sorte que le nom de l’instance de service n’a pas besoin d’inclure un nom d’hôte.

 

 



