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
# <a name="group-clause"></a><span data-ttu-id="69978-103">GROUP, clause</span><span class="sxs-lookup"><span data-stu-id="69978-103">GROUP Clause</span></span>

<span data-ttu-id="69978-104">La clause GROUP permet à WMI de générer une notification unique pour représenter un groupe d’événements.</span><span class="sxs-lookup"><span data-stu-id="69978-104">The GROUP clause causes WMI to generate a single notification to represent a group of events.</span></span> <span data-ttu-id="69978-105">La notification représentative est une instance de la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="69978-105">The representative notification is an instance of the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span> <span data-ttu-id="69978-106">La classe système **\_ \_ AggregateEvent** contient deux propriétés : **Representative** et **NumberOfEvents**.</span><span class="sxs-lookup"><span data-stu-id="69978-106">The **\_\_AggregateEvent** system class contains two properties: **Representative** and **NumberOfEvents**.</span></span> <span data-ttu-id="69978-107">La propriété **représentative** est un objet incorporé qui contient l’une des instances reçues pendant l’intervalle de regroupement spécifié dans la [clause within](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="69978-107">The **Representative** property is an embedded object that contains one of the instances received during the grouping interval specified in the [WITHIN clause](within-clause.md).</span></span> <span data-ttu-id="69978-108">Par exemple, si un événement d’agrégation est généré pour notifier des événements de modification d’instance, **Representative** contient une instance de la classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) .</span><span class="sxs-lookup"><span data-stu-id="69978-108">For example, if an aggregate event is generated to notify of instance modification events, **Representative** contains one instance of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) class.</span></span> <span data-ttu-id="69978-109">La propriété **NumberOfEvents** contient le nombre d’événements reçus pendant l’intervalle de regroupement.</span><span class="sxs-lookup"><span data-stu-id="69978-109">The **NumberOfEvents** property contains the number of events received during the grouping interval.</span></span> <span data-ttu-id="69978-110">L’intervalle de regroupement spécifie la période qui s’est écoulée après la réception d’un événement initial, pendant laquelle WMI doit collecter des événements similaires.</span><span class="sxs-lookup"><span data-stu-id="69978-110">The grouping interval specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span>

<span data-ttu-id="69978-111">La clause GROUP doit contenir une clause WITHIN pour spécifier l’intervalle de regroupement et peut contenir le mot clé BY ou HAVING, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="69978-111">The GROUP clause must contain a WITHIN clause to specify the grouping interval and can contain the BY or HAVING keyword, or both.</span></span> <span data-ttu-id="69978-112">La clause GROUP est placée après la clause WHERE, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="69978-112">The GROUP clause is placed after the WHERE clause, as shown following:</span></span>

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

<span data-ttu-id="69978-113">La valeur *EventClass* est la classe d’événements dont l’événement est membre, et *value* est la valeur de la propriété sur laquelle la notification est requise.</span><span class="sxs-lookup"><span data-stu-id="69978-113">The *EventClass* value is the event class of which the event is a member, and *value* is the value for the property on which notification is required.</span></span> <span data-ttu-id="69978-114">L’intervalle est un entier non signé qui représente l’intervalle de regroupement après la réception du premier événement.</span><span class="sxs-lookup"><span data-stu-id="69978-114">The interval is an unsigned integer that represents the grouping interval after receiving the first event.</span></span> <span data-ttu-id="69978-115">L’entier non signé est un nombre de secondes.</span><span class="sxs-lookup"><span data-stu-id="69978-115">The unsigned integer is a number of seconds.</span></span> <span data-ttu-id="69978-116">La liste de propriétés est une liste délimitée par des virgules d’une ou de plusieurs propriétés incluses dans la classe d’événements ; l' *opérateur* est un opérateur relationnel ; et *Integer* est un entier 32 bits non signé indiquant un nombre d’événements.</span><span class="sxs-lookup"><span data-stu-id="69978-116">The property list is a comma-delimited list of one or more properties that are included in the event class; *operator* is any relational operator; and *integer* is an unsigned 32-bit integer indicating a number of events.</span></span>

<span data-ttu-id="69978-117">Lors de l’utilisation de la clause GROUP, les clauses WHERE, BY et HAVING sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="69978-117">When using the GROUP clause, the WHERE, BY, and HAVING clauses are optional.</span></span>

<span data-ttu-id="69978-118">Une utilisation de base de la clause GROUP peut demander un regroupement d’événements dans un intervalle de temps qui commence lorsque le premier événement est reçu.</span><span class="sxs-lookup"><span data-stu-id="69978-118">A basic use of the GROUP clause might request a grouping of events within a time interval that starts when the first event is received.</span></span> <span data-ttu-id="69978-119">Par exemple, la requête suivante regroupe tous les événements de courrier électronique envoyés en moins de 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="69978-119">For example, the following query groups all of the email events sent within 5 minutes.</span></span> <span data-ttu-id="69978-120">Au lieu de paginer un utilisateur chaque fois qu’un message électronique est reçu, le consommateur permanent peut utiliser cette requête pour informer l’utilisateur uniquement si de nouveaux messages électroniques ont été reçus au cours des 5 dernières minutes.</span><span class="sxs-lookup"><span data-stu-id="69978-120">Instead of paging a user every time a piece of new email is received, the permanent consumer might use this query to inform the user only if new email has been received within the last 5 minutes.</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



<span data-ttu-id="69978-121">Si des informations plus détaillées sont requises, les événements peuvent être regroupés par une ou plusieurs propriétés de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="69978-121">If more detailed information is required, events can be grouped by one or more properties of the event class.</span></span> <span data-ttu-id="69978-122">La requête suivante demande que les événements de messagerie soient combinés avec d’autres événements qui ont la même valeur dans la propriété **sender** :</span><span class="sxs-lookup"><span data-stu-id="69978-122">The following query requests that email events be combined with other events that have the same value in the **Sender** property:</span></span>


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



<span data-ttu-id="69978-123">Un niveau de détail toujours plus élevé peut être obtenu en ajoutant une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="69978-123">A still greater level of detail can be achieved by adding a WHERE clause.</span></span> <span data-ttu-id="69978-124">Par exemple, la requête suivante notifie un utilisateur de nouveaux messages électroniques d’un expéditeur donné qui est arrivé au cours des 10 dernières minutes, combiné avec d’autres événements ayant la même valeur dans la propriété **importance** :</span><span class="sxs-lookup"><span data-stu-id="69978-124">For example, the following query notifies a user of new email from a particular sender that has arrived within the last 10 minutes, combined with other events that have the same value in the **Importance** property:</span></span>


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



