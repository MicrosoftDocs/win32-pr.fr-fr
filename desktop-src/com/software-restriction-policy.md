---
title: Stratégie de restriction logicielle
description: les paramètres de stratégie de restriction logicielle (SRP) ont été introduits avec la version de Windows XP pour aider à protéger les systèmes contre du code inconnu et potentiellement dangereux.
ms.assetid: 44b4e448-f5b4-4483-b53b-506938b36857
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97bf42cd949127e9012580ec16379cf36a95353
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294327"
---
# <a name="software-restriction-policy"></a>Stratégie de restriction logicielle

les paramètres de stratégie de restriction logicielle (SRP) ont été introduits avec la version de Windows XP pour aider à protéger les systèmes contre du code inconnu et potentiellement dangereux. Le SRP fournit un mécanisme dans lequel seul le code de confiance est autorisé à accéder de façon illimitée aux privilèges d’un utilisateur. Un code inconnu, qui peut contenir des virus ou du code qui est en conflit avec des programmes actuellement installés, est autorisé à s’exécuter uniquement dans un environnement restreint (souvent appelé *bac à sable (sandbox*)) où il n’est pas autorisé à accéder à des privilèges d’utilisateur sensibles à la sécurité. L’utilisation correcte du SRP peut rendre votre entreprise plus agile, car elle fournit une infrastructure proactive pour empêcher les problèmes, plutôt qu’une infrastructure réactive qui s’appuie sur l’alternative coûteuse de restauration d’un système après un problème.

Le SRP dépend de l’attribution de niveaux de confiance au code qui peut s’exécuter sur un système. Actuellement, il existe deux niveaux de confiance : non restreint et interdit. Le code ayant un niveau de confiance non restreint bénéficie d’un accès illimité aux privilèges de l’utilisateur. ce niveau de confiance ne doit donc être appliqué qu’à du code d’un niveau de confiance suffisant. Le code avec un niveau de confiance non autorisé n’est pas autorisé à accéder à des privilèges d’utilisateur sensibles à la sécurité et peut s’exécuter uniquement dans un bac à sable (sandbox), de sorte que le code non restreint ne peut pas charger le code non autorisé dans son espace d’adressage.

La configuration du SRP des applications COM individuelles s’effectue via la valeur [SRPTrustLevel](srptrustlevel.md) de la clé [AppID](appid-key.md) de l’application dans le registre. Si le niveau de confiance SRP n’est pas spécifié pour une application COM, la valeur par défaut interdit est utilisée. Une application COM disposant d’un niveau de confiance non restreint dispose d’un accès illimité aux privilèges de l’utilisateur, mais elle peut charger uniquement des composants avec un niveau de confiance illimité, tandis qu’une application COM non autorisée peut charger des composants avec n’importe quel niveau de confiance, mais ne peut pas accéder à des privilèges d’utilisateur sensibles à la sécurité.

Outre les niveaux de confiance du SRP des applications COM individuelles, deux autres propriétés de SRP déterminent la façon dont le SRP est utilisé pour toutes les applications COM. Si [SRPRunningObjectChecks](srprunningobjectchecks.md) est activé, les tentatives de connexion aux objets en cours d’exécution sont vérifiées pour les niveaux de confiance SRP appropriés. L’objet en cours d’exécution ne peut pas avoir un niveau de confiance SRP moins strict que l’objet client. Par exemple, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance non autorisé si l’objet client a un niveau de confiance illimité.

La deuxième propriété détermine la manière dont le SRP gère les connexions Activate-As-Activate. Si [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md) est activé, le niveau de confiance SRP configuré pour l’objet serveur est comparé au niveau de confiance SRP de l’objet client et le niveau de confiance le plus strict est utilisé pour exécuter l’objet serveur. Si **SRPActivateAsActivatorChecks** n’est pas activé, l’objet serveur s’exécute avec le niveau de confiance SRP de l’objet client, quel que soit le niveau de confiance du SRP avec lequel il a été configuré. Par défaut, **SRPRunningObjectChecks** et **SRPActivateAsActivatorChecks** sont activés.

 

 




