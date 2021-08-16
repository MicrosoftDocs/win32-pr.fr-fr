---
title: objectCategory et objectClass
description: Les attributs objectCategory et objectClass peuvent faire référence à une classe de schéma donnée d’un objet d’annuaire.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- interface ADSI de objectCategory et objectClass
- attributs ASI, recherche sur les attributs objectCategory et objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3833f8cf26cb2272fbe1e7c1063322f39a8c0147e4b22382d26067f90e72e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839219"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory et objectClass

Les attributs **objectCategory** et **objectClass** peuvent faire référence à une classe de schéma donnée d’un objet d’annuaire. Toutefois, il existe une distinction importante dans la sémantique entre les deux. « objectClass = Joy » fait référence à des objets de répertoire dans lesquels « Joy » représente toute classe dans la hiérarchie de classes d’objets. « objectCategory = Joy », en revanche, fait référence aux objets d’annuaire dans lesquels « Joy » identifie une classe spécifique dans la hiérarchie de classes d’objets.

**objectClass** peut prendre plusieurs valeurs, alors que **objectCategory** accepte une seule valeur. Pour cette raison, **objectCategory** est mieux adapté à la correspondance de type d’objets dans une recherche de répertoire. ADSI utilise ce critère comme critère de correspondance par défaut. Les recherches utilisant un **objectClass** ne sont pas évolutives pour les bases de données volumineuses. ADSI prend en charge les syntaxes « (objectCategory = SomeDN) » et « (objectCategory = LDAP \_ Display \_ name \_ of \_ Class) ».

La seule exception à cela est que le filtre de recherche LDAP « (objectClass = \* ) » ne spécifie pas de recherche sur la classe d’objet, mais teste simplement la présence des objets.

 

 




