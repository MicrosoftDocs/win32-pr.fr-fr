---
title: Principaux de sécurité
description: Dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur \ 8212 ; entité que le système de sécurité reconnaît.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- principaux de sécurité AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510389"
---
# <a name="security-principals"></a>Principaux de sécurité

Dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur, une entité que le système de sécurité reconnaît. Cela comprend les utilisateurs humains et les processus autonomes. Strictement parlant, le système de sécurité ne peut pas déterminer la différence entre les utilisateurs qui sont connectés et les processus en cours d’exécution sur l’ordinateur. Il voit à la fois comme entités de sécurité avec des noms de principal de sécurité.

Les utilisateurs, les groupes et les ordinateurs sont créés et stockés en tant qu’objets dans Active Directory Domain Services. Il existe également des principaux de sécurité connus qui représentent des identités spéciales définies par le système de sécurité de Windows 2000, telles que tout le monde, système local, principal Self, utilisateur authentifié, propriétaire créateur, et ainsi de suite. Les objets représentant les principaux de sécurité connus, tels que Anonymous Logon, sont stockés dans le conteneur WellKnown Security principals sous le conteneur Configuration.

 

 




