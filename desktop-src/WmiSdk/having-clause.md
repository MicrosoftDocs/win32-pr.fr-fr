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
# <a name="having-clause"></a><span data-ttu-id="ea35f-103">HAVING (clause)</span><span class="sxs-lookup"><span data-stu-id="ea35f-103">HAVING Clause</span></span>

<span data-ttu-id="ea35f-104">La clause HAVING est utilisée pour filtrer les événements reçus pendant l’intervalle de regroupement spécifié dans la [clause within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="ea35f-104">The HAVING clause is used to filter the events that are received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="ea35f-105">Par exemple, une instruction SELECT peut être construite pour ne retourner rien, sauf si au moins 5 événements se sont écoulés au cours du dernier intervalle de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="ea35f-105">For example, a SELECT statement could be constructed so that it returns nothing unless there HAVE been at least 5 events within the past 30 second INTERVAL.</span></span>

<span data-ttu-id="ea35f-106">La clause WITHIN suit immédiatement dans l' [instruction SELECT](select-statement-for-event-queries.md) après la clause [Group](group-clause.md) .</span><span class="sxs-lookup"><span data-stu-id="ea35f-106">The WITHIN clause follows immediately in the [SELECT statement](select-statement-for-event-queries.md) after the [GROUP](group-clause.md) clause.</span></span> <span data-ttu-id="ea35f-107">La clause HAVING fonctionne sur la propriété **NumberOfEvents** de la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) , dont le groupe créé par la clause Group est un membre.</span><span class="sxs-lookup"><span data-stu-id="ea35f-107">The HAVING clause operates on the **NumberOfEvents** property of the [**\_\_AggregateEvent**](--aggregateevent.md) system class, of which the group created by the GROUP clause is a member.</span></span> <span data-ttu-id="ea35f-108">La clause HAVING peut utiliser tous les opérateurs relationnels standard.</span><span class="sxs-lookup"><span data-stu-id="ea35f-108">The HAVING clause can use all of the standard relational operators.</span></span>

<span data-ttu-id="ea35f-109">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ea35f-109">The syntax is as follows:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

<span data-ttu-id="ea35f-110">La valeur *EventClass* est la classe d’événements dont l’événement est membre, et *value* est la valeur de la propriété sur laquelle la notification est requise.</span><span class="sxs-lookup"><span data-stu-id="ea35f-110">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="ea35f-111">L’intervalle est un entier non signé qui représente l’intervalle de regroupement (en secondes) après la réception du premier événement.</span><span class="sxs-lookup"><span data-stu-id="ea35f-111">The interval is an unsigned integer that represents the grouping interval (in seconds) after receiving the first event.</span></span> <span data-ttu-id="ea35f-112">La liste de propriétés est une liste délimitée par des virgules d’une ou de plusieurs propriétés incluses dans la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="ea35f-112">The property list is a comma-delimited list of one or more properties that are included in the event class.</span></span> <span data-ttu-id="ea35f-113">L’opérateur est un opérateur relationnel.</span><span class="sxs-lookup"><span data-stu-id="ea35f-113">The operator is any relational operator.</span></span> <span data-ttu-id="ea35f-114">La valeur de constante est un entier 32 bits non signé qui indique le nombre d’événements utilisés pour le filtrage.</span><span class="sxs-lookup"><span data-stu-id="ea35f-114">The constant value is any unsigned 32-bit integer indicating the number of events used for filtering.</span></span>

<span data-ttu-id="ea35f-115">Lors de l’utilisation de la clause HAVING, les clauses WHERE et BY sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="ea35f-115">When using the HAVING clause, the WHERE and BY clauses are optional.</span></span>

<span data-ttu-id="ea35f-116">La requête d’événement suivante demande que les notifications de la classe **EmailEvent** soient regroupées en un événement de 300 secondes après le premier événement reçu par WMI.</span><span class="sxs-lookup"><span data-stu-id="ea35f-116">The following event query requests that notifications of the **EmailEvent** class be grouped into one event 300 seconds after the first event that WMI receives.</span></span> <span data-ttu-id="ea35f-117">En outre, la requête demande l’instance [**\_ \_ AggregateEvent**](--aggregateevent.md) doit être remise uniquement si WMI reçoit plus de cinq événements de messagerie en 300 secondes.</span><span class="sxs-lookup"><span data-stu-id="ea35f-117">Also, the query requests the [**\_\_AggregateEvent**](--aggregateevent.md) instance should be delivered only if WMI receives more than five email events in that 300 seconds.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



<span data-ttu-id="ea35f-118">L’exemple suivant regroupe tous les événements reçus en 600 secondes (c’est-à-dire 10 minutes) par **TargetInstance**. Propriété **SourceName** .</span><span class="sxs-lookup"><span data-stu-id="ea35f-118">The following example groups all events received in 600 seconds (that is, 10 minutes) by the **TargetInstance**.**SourceName** property.</span></span> <span data-ttu-id="ea35f-119">Dans cet exemple, les événements d’agrégation sont remis uniquement si le nombre d’événements [**\_ NTLogEvent Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) reçus de la même source dépasse 25.</span><span class="sxs-lookup"><span data-stu-id="ea35f-119">In this example, aggregate events are delivered only if the number of [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) events received from the same source exceeds 25.</span></span> <span data-ttu-id="ea35f-120">Gardez à l’esprit que l’opérateur ISA fait en sorte que la propriété **TargetInstance** de la classe système [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) représente une instance de la classe **Win32 \_ NTLogEvent** .</span><span class="sxs-lookup"><span data-stu-id="ea35f-120">Keep in mind that the ISA operator causes the **TargetInstance** property of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) system class to represent an instance of the **Win32\_NTLogEvent** class.</span></span>


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
