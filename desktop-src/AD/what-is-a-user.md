---
title: Qu’est-ce qu’un utilisateur ?
description: Les comptes d’utilisateur sont créés et stockés en tant qu’objets dans Active Directory Domain Services.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- Qu’est-ce qu’un utilisateur Active Directory
- utilisateurs Active Directory, qu’est-ce qu’un utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5647caef184b1e2b18e7639f1540afde013a3ba33ab58adbd402296656ca44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024410"
---
# <a name="what-is-a-user"></a>Qu’est-ce qu’un utilisateur ?

Les comptes d’utilisateur sont créés et stockés en tant qu’objets dans Active Directory Domain Services. Les comptes d’utilisateur peuvent être utilisés par des utilisateurs humains ou des programmes, tels que les services système, pour se connecter à un ordinateur. Lorsqu’un utilisateur ouvre une session, le système vérifie le mot de passe de l’utilisateur en le comparant avec les données stockées dans l’objet utilisateur de l’utilisateur dans le serveur de Active Directory. Si le mot de passe est authentifié, autrement dit, le mot de passe présenté correspond au mot de passe stocké dans l’objet utilisateur, le système génère un jeton d’accès. Un jeton d’accès est un objet qui décrit le contexte de sécurité d’un processus ou d’un thread. Les données d’un jeton incluent l’identité de sécurité et les appartenances aux groupes du compte d’utilisateur associé au processus ou au thread. Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.

chaque utilisateur ou application qui accède à des ressources dans un domaine Windows doit avoir un compte sur le serveur Active Directory. Windows utilise ce compte d’utilisateur pour vérifier que l’utilisateur ou l’application a l’autorisation d’utiliser une ressource.

Un compte d’utilisateur peut être utilisé pour :

-   Permettre aux utilisateurs humains de se connecter à un ordinateur et d’accéder aux ressources en fonction de l’identité de ce compte d’utilisateur.
-   Permet aux programmes et aux services de s’exécuter dans un contexte de sécurité spécifique.
-   Gérez l’accès des utilisateurs aux ressources partagées, telles que les objets et leurs propriétés, les partages réseau, les fichiers, les répertoires, les files d’attente d’impression, etc.

Les groupes peuvent contenir des membres, qui sont des références à des utilisateurs et à d’autres groupes. Les groupes peuvent également être utilisés pour contrôler l’accès aux ressources partagées. Lorsque vous affectez des autorisations pour des ressources, par exemple des partages de fichiers, des imprimantes, etc., les administrateurs doivent attribuer ces autorisations à un groupe plutôt qu’à des utilisateurs individuels. Les autorisations sont affectées une seule fois au groupe, au lieu de plusieurs fois pour chaque utilisateur individuel. Cela permet de simplifier la maintenance et l’administration d’un réseau.

## <a name="users-compared-to-contacts"></a>Utilisateurs comparés aux contacts

Les utilisateurs et les contacts peuvent être utilisés pour représenter des utilisateurs humains. Toutefois, un utilisateur est un principal de sécurité ; un contact n’est pas.

Un utilisateur peut être utilisé pour permettre à un utilisateur humain de se connecter et d’accéder à des ressources partagées.

Un contact est utilisé uniquement à des fins de liste de distribution et de courrier électronique. Toutefois, un contact peut contenir la plupart des données stockées dans un objet utilisateur, telles que l’adresse, les numéros de téléphone, etc., car l’utilisateur et le contact sont tous deux dérivés de l’objet de la personne **classSchema** . Un contact n’a pas de contexte de sécurité ; par conséquent, un contact ne peut pas être utilisé pour contrôler l’accès aux ressources partagées et ne peut pas être utilisé pour se connecter à un ordinateur.

## <a name="users-compared-to-computers"></a>Utilisateurs comparés aux ordinateurs

La classe d’objet ordinateur hérite de la classe d’objet utilisateur. Un objet ordinateur représente un ordinateur ; Toutefois, l’ordinateur et les services locaux de l’ordinateur requièrent souvent l’accès au réseau et aux ressources partagées. Lorsque l’ordinateur accède à des ressources partagées, et non à l’utilisateur connecté à l’ordinateur, il a besoin d’un jeton d’accès de la même manière qu’un utilisateur humain connecté en tant qu’utilisateur. Lorsqu’un ordinateur accède au réseau, il utilise un jeton d’accès qui contient l’identificateur de sécurité pour le compte d’ordinateur de l’ordinateur et les groupes dont ce compte est membre.

Un service peut s’exécuter dans le contexte de LocalSystem ou d’un compte de service spécifique. sur les ordinateurs qui exécutent Windows 2000, un service qui s’exécute dans le contexte du compte LocalSystem utilise les informations d’identification de l’ordinateur.

 

 




