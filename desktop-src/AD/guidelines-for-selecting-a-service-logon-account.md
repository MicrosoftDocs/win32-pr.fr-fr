---
title: Instructions pour la sélection d’un compte d’ouverture de session de service
description: Un service Win32 peut s’exécuter dans le contexte de sécurité d’un compte d’utilisateur local, d’un compte d’utilisateur de domaine ou du compte LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Instructions pour la sélection d’un compte d’ouverture de session de service AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028606"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Instructions pour la sélection d’un compte d’ouverture de session de service

Un service Win32 peut s’exécuter dans le contexte de sécurité d’un compte d’utilisateur local, d’un compte d’utilisateur de domaine ou du compte LocalSystem. Pour déterminer le compte à utiliser, un administrateur doit installer le service avec le jeu d’autorisations minimal requis pour effectuer les opérations de service. Dans un service standard d’annuaire, cela signifie que le programme d’installation du service doit créer un compte d’utilisateur de domaine pour le service et accorder à ce compte les droits d’accès et les privilèges spécifiques requis par le service au moment de l’exécution. Un service ne doit s’exécuter que sous le compte LocalSystem si le service requiert des privilèges d’administrateur ou s’il doit agir en tant que partie du système d’exploitation sur l’ordinateur local.

N’oubliez pas que le programme d’installation du service doit, par défaut, configurer le service pour qu’il s’exécute sous un compte d’utilisateur de domaine. Pour exécuter le service sous le compte LocalSystem, le programme d’installation du service doit demander à l’administrateur l’autorisation de le faire.

Pour plus d’informations sur les descriptions, les avantages et les inconvénients de chaque type de compte, consultez :

-   [Comptes d’utilisateurs locaux](local-user-accounts.md).
-   [Comptes d’utilisateur de domaine](domain-user-accounts.md).
-   [Compte LocalSystem](the-localsystem-account.md).

 

 




