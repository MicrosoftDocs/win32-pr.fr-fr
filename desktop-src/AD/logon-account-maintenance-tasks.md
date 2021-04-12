---
title: Tâches de maintenance du compte d’ouverture de session
description: Cette rubrique décrit les problèmes liés aux tâches de maintenance de compte d’ouverture de session.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- Tâches de maintenance de compte d’ouverture de session Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104381761"
---
# <a name="logon-account-maintenance-tasks"></a>Tâches de maintenance du compte d’ouverture de session

Cette rubrique décrit les problèmes liés aux tâches de maintenance de compte d’ouverture de session.

Il existe deux problèmes principaux qui concernent les tâches de maintenance de compte d’ouverture de session :

-   Mise à jour du mot de passe du compte pour une instance de service qui s’exécute sous un compte d’utilisateur. Pour plus d’informations, consultez [modification du mot de passe sur le compte d’utilisateur d’un service](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Gestion des modifications apportées au compte d’ouverture de session d’une instance de service.

Ce dernier cas est rare, mais peut se produire. Le système fournit l’outil d’administration gestion de l’ordinateur qui permet la modification d’un compte d’ouverture de session de service. En outre, d’autres applications peuvent utiliser la fonction [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) pour spécifier un nouveau compte d’ouverture de session pour un service installé. Par défaut, des privilèges d’administrateur local sont requis pour modifier un compte de service. Si cela s’est produit, cela peut affecter votre service de deux manières :

-   Si vous avez inscrit des noms de principal du service (SPN), ceux-ci seront inscrits sur le mauvais compte.
-   Si vous définissez des ACE pour accorder l’accès au service, ils accordent à présent l’accès au mauvais compte.

Une approche consiste à faire en sorte que le programme d’installation du service stocke les noms de principal du service inscrits pour chaque instance de service dans le registre de l’ordinateur hôte. Vous pouvez utiliser la même clé de Registre sous HKEY \_ local \_ machine que celle utilisée pour stocker la chaîne de liaison pour le SCP du service. Lorsque le service démarre, il appelle la fonction [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) pour déterminer son compte d’ouverture de session, puis interroge le serveur Active Directory pour déterminer si les noms principaux de service sont inscrits sur l’objet d’annuaire pour ce compte. Si les noms de principal du service ne sont pas inscrits ou s’ils sont inscrits sur un compte incorrect, le service refuse de démarrer et affiche un message indiquant qu’un administrateur de domaine doit exécuter le programme de configuration du service pour mettre à jour les paramètres du compte d’ouverture de session. N’oubliez pas que cette reconfiguration doit être effectuée par un administrateur, car le compte de service ne doit pas avoir accès pour mettre à jour son propre SPN. Sachez également que les noms de principal du service doivent être supprimés de l’ancien compte. dans le cas contraire, les SPN seront inutiles pour l’authentification, car ils ne sont pas uniques dans la forêt.

 

 