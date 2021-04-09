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
# <a name="within-clause"></a><span data-ttu-id="68b5a-103">Clause WITHIN</span><span class="sxs-lookup"><span data-stu-id="68b5a-103">WITHIN Clause</span></span>

<span data-ttu-id="68b5a-104">Les consommateurs d’événements utilisent la clause WITHIN dans des requêtes d’événements pour spécifier une fréquence d' *interrogation* ou un *intervalle de regroupement*.</span><span class="sxs-lookup"><span data-stu-id="68b5a-104">Event consumers use the WITHIN clause in event queries to specify a *polling interval* or a *grouping interval*.</span></span>

<span data-ttu-id="68b5a-105">L’intervalle d’interrogation est l’intervalle que Windows Management Instrumentation (WMI) utilise pour interroger le fournisseur de données responsable de la classe pour les [événements intrinsèques](determining-the-type-of-event-to-receive.md)dont l’événement interrogé est membre.</span><span class="sxs-lookup"><span data-stu-id="68b5a-105">A polling interval is the interval that Windows Management Instrumentation (WMI) uses to poll the data provider responsible for the class for [intrinsic events](determining-the-type-of-event-to-receive.md), of which the event queried is a member.</span></span> <span data-ttu-id="68b5a-106">Cet intervalle est la durée maximale qui peut s'écouler avant que la notification d'un événement soit transmise.</span><span class="sxs-lookup"><span data-stu-id="68b5a-106">This interval is the maximum amount of time that can pass before notification of an event must be delivered.</span></span> <span data-ttu-id="68b5a-107">Un consommateur utilise un intervalle d’interrogation dans une clause WITHIN lorsque le consommateur requiert la notification des modifications apportées à une classe et qu’un fournisseur d’événements n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="68b5a-107">A consumer uses a polling interval in a WITHIN clause when the consumer requires notification of changes to a class, and an event provider is unavailable.</span></span> <span data-ttu-id="68b5a-108">Le consommateur s’inscrit pour un événement intrinsèque et comprend l’intervalle d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="68b5a-108">The consumer registers for an intrinsic event and includes the polling interval.</span></span>

<span data-ttu-id="68b5a-109">Pour spécifier une fréquence d’interrogation, placez la clause WITHIN immédiatement avant la clause WHERE, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="68b5a-109">To specify a polling interval, place the WITHIN clause immediately before the WHERE clause, as shown following:</span></span>


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



<span data-ttu-id="68b5a-110">IntrinsicEventClass est la classe d’événements intrinsèque dont l’événement est membre, interval est l’intervalle d’interrogation et value est la valeur de la propriété sur laquelle le consommateur requiert une notification.</span><span class="sxs-lookup"><span data-stu-id="68b5a-110">IntrinsicEventClass is the intrinsic event class of which the event is a member, interval is the polling interval, and value is the value for the property on which the consumer requires notification.</span></span>

<span data-ttu-id="68b5a-111">L’intervalle d’interrogation est un nombre à virgule flottante et peut être fractionnaire pour accepter des valeurs inférieures à 1 seconde.</span><span class="sxs-lookup"><span data-stu-id="68b5a-111">The polling interval is a floating-point number, and can be fractional to accept values smaller than 1 second.</span></span> <span data-ttu-id="68b5a-112">Toutefois, l’intervalle doit représenter un nombre de secondes plutôt qu’une très petite valeur, telle que 0,001, car la spécification d’une valeur trop petite peut entraîner la rejet par WMI de l’instruction comme non valide, en raison de la nature intensive de l’interrogation des ressources.</span><span class="sxs-lookup"><span data-stu-id="68b5a-112">However, the interval should represent a number of seconds rather than an extremely small value such as 0.001, because specifying a value that is too small can cause WMI to reject the statement as not valid—due to the resource-intensive nature of polling.</span></span> <span data-ttu-id="68b5a-113">La plupart des consommateurs d’événements ne nécessitant pas de notification immédiate, il est recommandé d’utiliser un intervalle supérieur à 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="68b5a-113">Because most event consumers do not require immediate notification, it is recommended that they use an interval that is greater than 5 minutes.</span></span>

<span data-ttu-id="68b5a-114">L’exemple de requête suivant demande à WMI de vérifier toutes les 10 secondes les modifications apportées aux instances de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="68b5a-114">The following query example requests that WMI check every 10 seconds for changes that occur to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span> <span data-ttu-id="68b5a-115">Si une instance de la classe est modifiée dans l’intervalle d’interrogation spécifié, un événement de notification est envoyé pour chaque modification.</span><span class="sxs-lookup"><span data-stu-id="68b5a-115">If an instance of the class is modified within the specified polling interval, a notification event is sent for each modification.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="68b5a-116">Selon la requête, un fournisseur d’événements et WMI peut partager la tâche de fourniture d’événements.</span><span class="sxs-lookup"><span data-stu-id="68b5a-116">Depending on the query, an event provider and WMI can share the task of providing events.</span></span> <span data-ttu-id="68b5a-117">Par exemple, un fournisseur d’événements qui prend en charge les événements des classes système [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) et [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , et non les événements de la classe système [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) .</span><span class="sxs-lookup"><span data-stu-id="68b5a-117">For example, an event provider that supports events of the [**\_\_InstanceCreationEvent**](--instancecreationevent.md) and [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system classes, and not events of the [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) system class.</span></span> <span data-ttu-id="68b5a-118">La requête suivante permet au fournisseur d’événements de générer les événements de création et de modification au fur et à mesure qu’ils se produisent et qu’ils sont remis lorsqu’ils sont créés.</span><span class="sxs-lookup"><span data-stu-id="68b5a-118">The following query enables the event provider to generate the creation and modification events as they occur and have them delivered when they are created.</span></span> <span data-ttu-id="68b5a-119">La requête permet également à WMI de générer des événements **\_ \_ InstanceDeletionEvent** toutes les 10 (dix) secondes à l’aide du mécanisme d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="68b5a-119">The query also allows WMI to generate **\_\_InstanceDeletionEvent** events every 10 (ten) seconds using the polling mechanism.</span></span>


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



<span data-ttu-id="68b5a-120">Vous pouvez également utiliser la clause WITHIN pour spécifier un intervalle de regroupement.</span><span class="sxs-lookup"><span data-stu-id="68b5a-120">You can also use the WITHIN clause to specify a grouping interval.</span></span> <span data-ttu-id="68b5a-121">Un intervalle de regroupement est un entier 32 bits non signé qui spécifie la période, après réception d’un événement initial, pendant laquelle WMI doit collecter des événements similaires.</span><span class="sxs-lookup"><span data-stu-id="68b5a-121">A grouping interval is an unsigned 32-bit integer that specifies the time period, after receiving an initial event, during which WMI should collect similar events.</span></span> <span data-ttu-id="68b5a-122">Lorsque ce délai expire, WMI remet l’événement d’agrégation, constitué de tous les événements similaires.</span><span class="sxs-lookup"><span data-stu-id="68b5a-122">When this time period expires, WMI delivers the aggregate event, made up of all the similar events.</span></span> <span data-ttu-id="68b5a-123">Pour plus d’informations, consultez [Group, clause](group-clause.md).</span><span class="sxs-lookup"><span data-stu-id="68b5a-123">For more information, see [GROUP Clause](group-clause.md).</span></span>

<span data-ttu-id="68b5a-124">Les consommateurs d’événements qui s’inscrivent à des événements fréquents utilisent un intervalle de regroupement avec la clause WITHIN.</span><span class="sxs-lookup"><span data-stu-id="68b5a-124">Event consumers that register for frequently occurring events use a grouping interval with the WITHIN clause.</span></span> <span data-ttu-id="68b5a-125">L’ajout d’un groupe au sein de la clause WHERE dans une requête d’événement entraîne l’envoi par WMI d’un événement d’agrégation plutôt que de nombreux événements.</span><span class="sxs-lookup"><span data-stu-id="68b5a-125">Adding GROUP WITHIN to the WHERE clause in an event query results in WMI sending one aggregate event rather than many events.</span></span> <span data-ttu-id="68b5a-126">L’événement Aggregate est représenté par la classe système [**\_ \_ AggregateEvent**](--aggregateevent.md) .</span><span class="sxs-lookup"><span data-stu-id="68b5a-126">The aggregate event is represented by the [**\_\_AggregateEvent**](--aggregateevent.md) system class.</span></span>

<span data-ttu-id="68b5a-127">Pour spécifier un intervalle de regroupement, placez la clause WITHIN immédiatement après la clause GROUP.</span><span class="sxs-lookup"><span data-stu-id="68b5a-127">To specify a grouping interval, place the WITHIN clause immediately after the GROUP clause.</span></span>


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



<span data-ttu-id="68b5a-128">EventClass est la classe d’événements dont l’événement est un membre, value est la valeur de la propriété sur laquelle le consommateur requiert une notification et interval est l’intervalle de regroupement.</span><span class="sxs-lookup"><span data-stu-id="68b5a-128">EventClass is the event class of which the event is a member, value is the value for the property on which the consumer requires notification, and Interval is the grouping interval.</span></span>

<span data-ttu-id="68b5a-129">Pour plus d’informations, consultez [détermination du type d’événement à recevoir](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="68b5a-129">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="68b5a-130">Les consommateurs d’événements permanents peuvent être créés avec des requêtes d’interrogation uniquement si vous disposez de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="68b5a-130">Permanent event consumers can be created with polling queries only if you have administrator privileges.</span></span>

 

 
