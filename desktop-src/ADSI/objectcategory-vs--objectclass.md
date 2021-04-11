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
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028557"
---
# <a name="objectcategory-vs-objectclass"></a>objectCategory et objectClass

Les attributs **objectCategory** et **objectClass** peuvent faire référence à une classe de schéma donnée d’un objet d’annuaire. Toutefois, il existe une distinction importante dans la sémantique entre les deux. « objectClass = Joy » fait référence à des objets de répertoire dans lesquels « Joy » représente toute classe dans la hiérarchie de classes d’objets. « objectCategory = Joy », en revanche, fait référence aux objets d’annuaire dans lesquels « Joy » identifie une classe spécifique dans la hiérarchie de classes d’objets.

**objectClass** peut prendre plusieurs valeurs, alors que **objectCategory** accepte une seule valeur. Pour cette raison, **objectCategory** est mieux adapté à la correspondance de type d’objets dans une recherche de répertoire. ADSI utilise ce critère comme critère de correspondance par défaut. Les recherches utilisant un **objectClass** ne sont pas évolutives pour les bases de données volumineuses. ADSI prend en charge les syntaxes « (objectCategory = SomeDN) » et « (objectCategory = LDAP \_ Display \_ name \_ of \_ Class) ».

La seule exception à cela est que le filtre de recherche LDAP « (objectClass = \* ) » ne spécifie pas de recherche sur la classe d’objet, mais teste simplement la présence des objets.

 

 




