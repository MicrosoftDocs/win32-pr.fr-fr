---
title: Principaux de sécurité
description: dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur \ 8212 ; entité que le système de sécurité reconnaît.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- principaux de sécurité AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d2c0e1bc36ce29e902b589541219760aa20cdfdbf4ebed7b570a01f707cb75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183907"
---
# <a name="security-principals"></a>Principaux de sécurité

dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur, une entité que le système de sécurité reconnaît. Cela comprend les utilisateurs humains et les processus autonomes. Strictement parlant, le système de sécurité ne peut pas déterminer la différence entre les utilisateurs qui sont connectés et les processus en cours d’exécution sur l’ordinateur. Il voit à la fois comme entités de sécurité avec des noms de principal de sécurité.

Les utilisateurs, les groupes et les ordinateurs sont créés et stockés en tant qu’objets dans Active Directory Domain Services. il existe également des principaux de sécurité connus qui représentent des identités spéciales définies par le système de sécurité Windows 2000, telles que tout le monde, système Local, Self-Principal, utilisateur authentifié, propriétaire créateur, et ainsi de suite. Les objets représentant les principaux de sécurité connus, tels que Anonymous Logon, sont stockés dans le conteneur WellKnown Security principals sous le conteneur Configuration.

 

 




