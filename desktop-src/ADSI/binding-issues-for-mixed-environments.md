---
title: Problèmes de liaison pour les environnements mixtes
description: Problèmes de liaison pour les environnements mixtes
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, avec, problèmes de liaison pour les environnements mixtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509059"
---
# <a name="binding-issues-for-mixed-environments"></a>Problèmes de liaison pour les environnements mixtes

Pour les environnements dans lesquels le domaine qui contient Active Directory a une relation d’approbation avec un domaine Windows NT 4,0, il peut y avoir un problème avec l’utilisation de la liaison sans serveur pour la liaison à des objets Active Directory.

Dans certains environnements réseau, les relations d’approbation ont été configurées entre les contrôleurs de domaine qui contiennent des Active Directory et des serveurs Windows NT 4,0 afin d’autoriser l’authentification entre les domaines. Dans ces environnements mixtes, si un utilisateur qui est membre du Windows NT 4,0, le domaine tente d’utiliser une liaison sans serveur pour établir une liaison à un objet Active Directory sur un domaine approuvé, la liaison échoue et une erreur est retournée. Cela est dû au fait qu’une liaison sans serveur utilise la fonction [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) pour établir une liaison à l’objet dans Active Directory, qui dépend du DNS approprié.

Dans ce scénario, l’utilisateur Windows NT doit fournir le nom d’un domaine spécifique auquel effectuer la liaison. Voici un exemple.

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 