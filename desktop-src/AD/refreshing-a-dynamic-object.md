---
title: Actualisation d’un objet dynamique
description: Un client peut actualiser la durée de vie (TTL, Time to Live) d’une entrée de répertoire donnée pour la maintenir active de l’une des deux façons d’effectuer une mise à jour LDAP sur la valeur de son attribut entryTTL avant que l’entrée ne soit récupérée par le garbage collector.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025175"
---
# <a name="refreshing-a-dynamic-object"></a>Actualisation d’un objet dynamique

Un client peut actualiser la durée de vie (TTL) d’une entrée de répertoire donnée pour la garder active de deux manières :

-   Exécution d’une mise à jour LDAP de la valeur de son attribut **entryTTL** avant que l’entrée ne soit récupérée par le garbage collector. Cette méthode d’actualisation d’une entrée dynamique dans l’annuaire est une fonctionnalité supplémentaire (facultative) de Active Directory Domain Services qui n’est pas spécifiée par la RFC 2589.
-   Exécution d’une opération LDAP étendue avec un OID de 1.3.6.1.4.1.1466.101.119.1 pour l’actualisation de la durée de vie, comme stipulé dans le document RFC 2589. Cet OID est défini comme **LDAP \_ TTL \_ Extended \_ op \_ OID** dans WINLDAP. H.

 
* * ReMark * * * : les objets dynamiques sont supprimés par le garbage collector lorsqu’ils ont expiré, aucune phase de l’objet n’est un objet tombstone lorsqu’il a expiré. Vous devez faire attention à la latence de réplication Active Directory lorsque vous actualisez des objets. Vous devez vous assurer que la mise à jour pour actualiser la durée de vie arrive suffisamment tôt pour que tous les réplicas du contexte d’appellation (catalogue complet et catalogue global) voient la transaction d’actualisation avant l’expiration locale de l’objet.

 




