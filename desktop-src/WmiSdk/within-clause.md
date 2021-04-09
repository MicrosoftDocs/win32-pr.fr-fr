---
description: Utilisez la clause WITHIN dans les requêtes d’événements pour spécifier une fréquence d’interrogation ou un intervalle de regroupement.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Clause WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d863e2e71d52fe60aeed7697feeb1231164c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115035"
---
# <a name="within-clause"></a>Clause WITHIN

Les consommateurs d’événements utilisent la clause WITHIN dans des requêtes d’événements pour spécifier une fréquence d' *interrogation* ou un *intervalle de regroupement*.

L’intervalle d’interrogation est l’intervalle que Windows Management Instrumentation (WMI) utilise pour interroger le fournisseur de données responsable de la classe pour les [événements intrinsèques](determining-the-type-of-event-to-receive.md)dont l’événement interrogé est membre. Cet intervalle est la durée maximale qui peut s'écouler avant que la notification d'un événement soit transmise. Un consommateur utilise un intervalle d’interrogation dans une clause WITHIN lorsque le consommateur requiert la notification des modifications apportées à une classe et qu’un fournisseur d’événements n’est pas disponible. Le consommateur s’inscrit pour un événement intrinsèque et comprend l’intervalle d’interrogation.

Pour spécifier une fréquence d’interrogation, placez la clause WITHIN immédiatement avant la clause WHERE, comme indiqué ci-dessous :


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass est la classe d’événements intrinsèque dont l’événement est membre, interval est l’intervalle d’interrogation et value est la valeur de la propriété sur laquelle le consommateur requiert une notification.

L’intervalle d’interrogation est un nombre à virgule flottante et peut être fractionnaire pour accepter des valeurs inférieures à 1 seconde. Toutefois, l’intervalle doit représenter un nombre de secondes plutôt qu’une très petite valeur, telle que 0,001, car la spécification d’une valeur trop petite peut entraîner la rejet par WMI de l’instruction comme non valide, en raison de la nature intensive de l’interrogation des ressources. La plupart des consommateurs d’événements ne nécessitant pas de notification immédiate, il est recommandé d’utiliser un intervalle supérieur à 5 minutes.

L’exemple de requête suivant demande à WMI de vérifier toutes les 10 secondes les modifications apportées aux instances de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Si une instance de la classe est modifiée dans l’intervalle d’interrogation spécifié, un événement de notification est envoyé pour chaque modification.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Selon la requête, un fournisseur d’événements et WMI peut partager la tâche de fourniture d’événements. Par exemple, un fournisseur d’événements qui prend en charge les événements des classes système [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) et [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , et non les événements de la classe système [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) . La requête suivante permet au fournisseur d’événements de générer les événements de création et de modification au fur et à mesure qu’ils se produisent et qu’ils sont remis lorsqu’ils sont créés. La requête permet également à WMI de générer des événements **\_ \_ InstanceDeletionEvent** toutes les 10 (dix) secondes à l’aide du mécanisme d’interrogation.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



Vous pouvez également utiliser la clause WITHIN pour spécifier un intervalle de regroupement. Un intervalle de regroupement est un entier 32 bits non signé qui spécifie la période, après réception d’un événement initial, pendant laquelle WMI doit collecter des événements similaires. Lorsque ce délai expire, WMI remet l’événement d’agrégation, constitué de tous les événements similaires. Pour plus d’informations, consultez [Group, clause](group-clause.md).

Les consommateurs d’événements qui s’inscrivent à des événements fréquents utilisent un intervalle de regroupement avec la clause WITHIN. L’ajout d’un groupe au sein de la clause WHERE dans une requête d’événement entraîne l’envoi par WMI d’un événement d’agrégation plutôt que de nombreux événements. L’événement Aggregate est représenté par la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) .

Pour spécifier un intervalle de regroupement, placez la clause WITHIN immédiatement après la clause GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass est la classe d’événements dont l’événement est un membre, value est la valeur de la propriété sur laquelle le consommateur requiert une notification et interval est l’intervalle de regroupement.

Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).

Les consommateurs d’événements permanents peuvent être créés avec des requêtes d’interrogation uniquement si vous disposez de privilèges d’administrateur.

 

 
