---
title: Partitions de l’annuaire d’applications
description: Dans Windows Server 2003, Active Directory Domain Services prendre en charge les partitions d’annuaire d’applications.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Partitions de l’annuaire d’applications Active Directory
- Partitions de l’annuaire d’applications Active Directory, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031055"
---
# <a name="application-directory-partitions"></a>Partitions de l’annuaire d’applications

Dans Windows Server 2003, Active Directory Domain Services prendre en charge les partitions d’annuaire d’applications. Une partition d’annuaire d’applications peut contenir une hiérarchie de tout type d’objets, à l’exception des principaux de sécurité, et peut être configurée pour répliquer sur n’importe quel ensemble de contrôleurs de domaine dans la forêt. Contrairement à une partition de domaine, il n’est pas nécessaire qu’une partition d’annuaire d’applications soit répliquée sur tous les contrôleurs de domaine d’un domaine, et la partition peut être répliquée sur des contrôleurs de domaine dans différents domaines de la forêt. Pour plus d’informations sur les partitions de l’annuaire d’applications, consultez [à propos des partitions de l’annuaire d’applications](about-application-directory-partitions.md).

Une partition d’annuaire d’applications peut être créée. modifié et supprimé à l’aide des opérations ADSI standard, LDAP et [System. DirectoryServices](/dotnet/api/system.directoryservices) . Le contexte de sécurité requis pour créer et modifier une partition d’annuaire d’applications est le même que pour la création d’une partition de domaine.

Les rubriques suivantes décrivent comment utiliser les partitions d’annuaire d’applications :

-   [Réplication de la partition de l’annuaire d’applications](application-directory-partition-replication.md)
-   [Sécurité de la partition de l’annuaire d’applications](application-directory-partition-security.md)
-   [Création d’une partition d’annuaire d’applications](creating-an-application-directory-partition.md)
-   [Suppression d’une partition d’annuaire d’applications](deleting-an-application-directory-partition.md)
-   [Énumération des partitions d’annuaire d’applications dans une forêt](enumerating-application-directory-partitions-in-a-forest.md)
-   [Localisation d’un serveur hôte de partition d’annuaire d’applications](locating-an-application-directory-partition-host-server.md)
-   [Ajout ou suppression d’un réplica de partition d’annuaire d’applications](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Énumération des réplicas d’une partition d’annuaire d’applications](enumerating-replicas-of-an-application-directory-partition.md)
-   [Modification de la configuration de la partition d’annuaire d’applications](modifying-application-directory-partition-configuration.md)

 

 