---
description: La clause GROUP permet à WMI de générer une notification unique pour représenter un groupe d’événements.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: GROUP, clause
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545104"
---
# <a name="group-clause"></a>GROUP, clause

La clause GROUP permet à WMI de générer une notification unique pour représenter un groupe d’événements. La notification représentative est une instance de la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) . La classe système **\_ \_ AggregateEvent** contient deux propriétés : **Representative** et **NumberOfEvents**. La propriété **représentative** est un objet incorporé qui contient l’une des instances reçues pendant l’intervalle de regroupement spécifié dans la [clause within](within-clause.md). Par exemple, si un événement d’agrégation est généré pour notifier des événements de modification d’instance, **Representative** contient une instance de la classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) . La propriété **NumberOfEvents** contient le nombre d’événements reçus pendant l’intervalle de regroupement. L’intervalle de regroupement spécifie la période qui s’est écoulée après la réception d’un événement initial, pendant laquelle WMI doit collecter des événements similaires.

La clause GROUP doit contenir une clause WITHIN pour spécifier l’intervalle de regroupement et peut contenir le mot clé BY ou HAVING, ou les deux. La clause GROUP est placée après la clause WHERE, comme indiqué ci-dessous :

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

La valeur *EventClass* est la classe d’événements dont l’événement est membre, et *value* est la valeur de la propriété sur laquelle la notification est requise. L’intervalle est un entier non signé qui représente l’intervalle de regroupement après la réception du premier événement. L’entier non signé est un nombre de secondes. La liste de propriétés est une liste délimitée par des virgules d’une ou de plusieurs propriétés incluses dans la classe d’événements ; l' *opérateur* est un opérateur relationnel ; et *Integer* est un entier 32 bits non signé indiquant un nombre d’événements.

Lors de l’utilisation de la clause GROUP, les clauses WHERE, BY et HAVING sont facultatives.

Une utilisation de base de la clause GROUP peut demander un regroupement d’événements dans un intervalle de temps qui commence lorsque le premier événement est reçu. Par exemple, la requête suivante regroupe tous les événements de courrier électronique envoyés en moins de 5 minutes. Au lieu de paginer un utilisateur chaque fois qu’un message électronique est reçu, le consommateur permanent peut utiliser cette requête pour informer l’utilisateur uniquement si de nouveaux messages électroniques ont été reçus au cours des 5 dernières minutes.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Si des informations plus détaillées sont requises, les événements peuvent être regroupés par une ou plusieurs propriétés de la classe d’événements. La requête suivante demande que les événements de messagerie soient combinés avec d’autres événements qui ont la même valeur dans la propriété **sender** :


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Un niveau de détail toujours plus élevé peut être obtenu en ajoutant une clause WHERE. Par exemple, la requête suivante notifie un utilisateur de nouveaux messages électroniques d’un expéditeur donné qui est arrivé au cours des 10 dernières minutes, combiné avec d’autres événements ayant la même valeur dans la propriété **importance** :


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



