---
title: À propos de la publication de service
description: Un service est une application qui rend des données ou des opérations disponibles pour les clients réseau. Souvent, un service est implémenté en tant que service formel basé sur Microsoft Win32, mais cela n’est pas obligatoire.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939544"
---
# <a name="about-service-publication"></a>À propos de la publication de service

Un service est une application qui rend des données ou des opérations disponibles pour les clients réseau. Souvent, un service est implémenté en tant que service formel basé sur Microsoft Win32, mais cela n’est pas obligatoire.

La publication de service consiste à créer et à gérer des données sur une ou plusieurs instances d’un service donné afin que les clients réseau puissent trouver et utiliser le service. La publication d’un service dans Active Directory Domain Services permet aux clients et aux administrateurs de passer d’une vue centrée sur l’ordinateur du système distribué à une vue orientée service.

**Systèmes d’exploitation Microsoft Windows NT 3,51 et versions ultérieures :** Un système distribué était un groupe d’ordinateurs qui exécutent divers services. Pour accéder à un service, une application nécessitait des données sur les ordinateurs qui ont proposé le service.

**Windows 2000 Server, windows 2000 Advanced Server et windows 2000 Datacenter Server :** Les services publient leur existence à l’aide d’objets Active Directory Domain Services. Les objets contiennent des informations de liaison que les applications clientes utilisent pour se connecter aux instances du service. Pour accéder à un service, un client n’a pas besoin d’en savoir plus sur des ordinateurs spécifiques : les objets d’un serveur Active Directory incluent ces informations. Un client interroge le serveur Active Directory pour obtenir un objet représentant un service (appelé objet point de connexion) et utilise les données de liaison de l’objet pour se connecter au service.

Le tableau suivant présente des exemples de liaisons.



| Service      | Liaison                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Service de fichiers | Nom UNC d’un partage. Par exemple \\ \\ , « MyServer \\ MyshareName ».                                                                                                                                                              |
| Service Web  | URL. Par exemple https://www.fabrikam.com , "".                                                                                                                                                                                 |
| Service RPC  | Liaison d’appel de procédure distante (RPC) : informations encodées spéciales utilisées pour la connexion au serveur RPC. Les liaisons RPC peuvent être converties vers et à partir de chaînes avec les API RPC. Par exemple : « ncacn \_ IP \_ TCP :Server. fabrikam. com ». |



 

Dans un système distribué, les ordinateurs sont des moteurs, et les entités intéressantes sont les services disponibles. Du point de vue de l’utilisateur, l’identité de l’ordinateur qui fournit un service particulier n’est pas importante. Ce qui est important, c’est d’accéder au service lui-même.

C’est également le cas avec la gestion des services. L’administrateur d’une zone DNS donnée n’est pas intéressé par les ordinateurs qui exécutent le service DNS. l’administrateur souhaite administrer DNS. Il y aura probablement plusieurs instances du service DNS, dont l’une fait autorité. Les ordinateurs qui prennent en charge le service DNS ne sont pas importants pour l’administrateur DNS. Il est important de savoir comment gérer le service comme une ressource distribuée unique, et non comme des processus individuels s’exécutant sur des ordinateurs différents.

 

 




