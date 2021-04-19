---
description: La clause HAVING est utilisée pour filtrer les événements reçus pendant l’intervalle de regroupement spécifié dans la clause WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: HAVING (clause)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f93fbe082fb2f655dfad59d7642e1d0ff9a33e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521183"
---
# <a name="having-clause"></a>HAVING (clause)

La clause HAVING est utilisée pour filtrer les événements reçus pendant l’intervalle de regroupement spécifié dans la [clause within](within-clause.md). Par exemple, une instruction SELECT peut être construite pour ne retourner rien, sauf si au moins 5 événements se sont écoulés au cours du dernier intervalle de 30 secondes.

La clause WITHIN suit immédiatement dans l' [instruction SELECT](select-statement-for-event-queries.md) après la clause [Group](group-clause.md) . La clause HAVING fonctionne sur la propriété **NumberOfEvents** de la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) , dont le groupe créé par la clause Group est un membre. La clause HAVING peut utiliser tous les opérateurs relationnels standard.

La syntaxe est la suivante :

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

La valeur *EventClass* est la classe d’événements dont l’événement est membre, et *value* est la valeur de la propriété sur laquelle la notification est requise. L’intervalle est un entier non signé qui représente l’intervalle de regroupement (en secondes) après la réception du premier événement. La liste de propriétés est une liste délimitée par des virgules d’une ou de plusieurs propriétés incluses dans la classe d’événements. L’opérateur est un opérateur relationnel. La valeur de constante est un entier 32 bits non signé qui indique le nombre d’événements utilisés pour le filtrage.

Lors de l’utilisation de la clause HAVING, les clauses WHERE et BY sont facultatives.

La requête d’événement suivante demande que les notifications de la classe **EmailEvent** soient regroupées en un événement de 300 secondes après le premier événement reçu par WMI. En outre, la requête demande l’instance [**\_ \_ AggregateEvent**](--aggregateevent.md) doit être remise uniquement si WMI reçoit plus de cinq événements de messagerie en 300 secondes.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



L’exemple suivant regroupe tous les événements reçus en 600 secondes (c’est-à-dire 10 minutes) par **TargetInstance**. Propriété **SourceName** . Dans cet exemple, les événements d’agrégation sont remis uniquement si le nombre d’événements [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) reçus de la même source dépasse 25. Gardez à l’esprit que l’opérateur ISA fait en sorte que la propriété **TargetInstance** de la classe système [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) représente une instance de la classe **Win32 \_ NTLogEvent** .


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
