---
description: Décrit la syntaxe de base d’une instruction SELECT pour les requêtes d’événement.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210204"
---
# <a name="select-statement-for-event-queries"></a><span data-ttu-id="186b4-103">Instruction SELECT pour les requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="186b4-103">SELECT Statement for Event Queries</span></span>

<span data-ttu-id="186b4-104">Vous pouvez utiliser diverses instructions SELECT pour rechercher des informations sur les événements.</span><span class="sxs-lookup"><span data-stu-id="186b4-104">You can use a variety of SELECT statements to query for event information.</span></span> <span data-ttu-id="186b4-105">Les instructions peuvent être des instructions de base ou elles peuvent être plus restrictives pour limiter le jeu de résultats retourné par la requête.</span><span class="sxs-lookup"><span data-stu-id="186b4-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="186b4-106">L’exemple suivant est une instruction SELECT de base qui est utilisée pour rechercher des informations sur les événements.</span><span class="sxs-lookup"><span data-stu-id="186b4-106">The following example is a basic SELECT statement that is used to query for event information.</span></span>


```sql
SELECT * FROM EventClass
```



<span data-ttu-id="186b4-107">Lorsqu’un consommateur envoie une requête, il s’agit d’une demande de notification de toutes les occurrences de l’événement représenté par **EventClass**.</span><span class="sxs-lookup"><span data-stu-id="186b4-107">When a consumer submits a query, it is a request to be notified of all occurrences of the event represented by **EventClass**.</span></span> <span data-ttu-id="186b4-108">Cette requête comprend une demande de notification concernant toutes les propriétés du système d’événements et non-système.</span><span class="sxs-lookup"><span data-stu-id="186b4-108">This request includes a request for notification about all of the event system and nonsystem properties.</span></span> <span data-ttu-id="186b4-109">Lorsqu’un fournisseur d’événements soumet une requête, il enregistre la prise en charge de la génération de notifications lorsqu’un événement représenté par **EventClass** se produit.</span><span class="sxs-lookup"><span data-stu-id="186b4-109">When an event provider submits a query, it registers support for generating notifications when an event represented by **EventClass** occurs.</span></span>

<span data-ttu-id="186b4-110">Les consommateurs peuvent spécifier des propriétés individuelles au lieu de l’astérisque ( \* ) dans l’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="186b4-110">Consumers can specify individual properties instead of the asterisk (\*) in the SELECT statement.</span></span>

<span data-ttu-id="186b4-111">L’exemple suivant montre comment interroger des propriétés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="186b4-111">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



<span data-ttu-id="186b4-112">Toutefois, toutes les propriétés d’un objet incorporé sont retournées, même si la requête spécifie des propriétés d’objet incorporées.</span><span class="sxs-lookup"><span data-stu-id="186b4-112">However, all of the properties of an embedded object are returned, even if the query specifies embedded object properties.</span></span>

<span data-ttu-id="186b4-113">L’exemple suivant montre deux requêtes qui retournent les mêmes données.</span><span class="sxs-lookup"><span data-stu-id="186b4-113">The following example shows two queries that return the same data.</span></span>


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



<span data-ttu-id="186b4-114">Si une propriété système n’est pas pertinente pour une requête spécifique, elle contient la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="186b4-114">If a system property is not relevant for a specific query, it contains **NULL**.</span></span> <span data-ttu-id="186b4-115">Par exemple, la valeur de la propriété système **\_ \_ RelPath** est **null** pour toutes les requêtes d’événement.</span><span class="sxs-lookup"><span data-stu-id="186b4-115">For example, the value of the **\_\_RELPATH** system property is **NULL** for all event queries.</span></span>

<span data-ttu-id="186b4-116">Les propriétés système suivantes contiennent la **valeur null** pour les requêtes d’événements :</span><span class="sxs-lookup"><span data-stu-id="186b4-116">The following system properties contain **NULL** for event queries:</span></span>

<dl> <span data-ttu-id="186b4-117">\_\_Joint</span><span class="sxs-lookup"><span data-stu-id="186b4-117">\_\_Namespace</span></span>  
<span data-ttu-id="186b4-118">\_\_D</span><span class="sxs-lookup"><span data-stu-id="186b4-118">\_\_Path</span></span>  
<span data-ttu-id="186b4-119">\_\_Constitue</span><span class="sxs-lookup"><span data-stu-id="186b4-119">\_\_RelPath</span></span>  
<span data-ttu-id="186b4-120">\_\_Serveurs</span><span class="sxs-lookup"><span data-stu-id="186b4-120">\_\_Server</span></span>  
</dl>

<span data-ttu-id="186b4-121">Pour plus d’informations, consultez [référence des propriétés système WMI](wmi-system-properties.md).</span><span class="sxs-lookup"><span data-stu-id="186b4-121">For more information, see [WMI System Property Reference](wmi-system-properties.md).</span></span>

<span data-ttu-id="186b4-122">Toutes les requêtes d’événements peuvent inclure une [clause WHERE](where-clause.md)facultative, mais les clauses WHERE sont principalement utilisées par les consommateurs pour spécifier un filtrage supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="186b4-122">All event queries can include an optional [WHERE clause](where-clause.md), but WHERE clauses are primarily used by consumers to specify additional filtering.</span></span> <span data-ttu-id="186b4-123">Il est fortement recommandé que les consommateurs spécifient toujours une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="186b4-123">It is strongly recommended that consumers always specify a WHERE clause.</span></span> <span data-ttu-id="186b4-124">Le coût d’une requête complexe est minime par rapport au coût de la diffusion et du traitement des notifications inutiles.</span><span class="sxs-lookup"><span data-stu-id="186b4-124">The cost of a complex query is minimal compared to the cost of delivering and processing unneeded notifications.</span></span>

<span data-ttu-id="186b4-125">L’exemple suivant montre une requête qui demande des notifications de tous les événements de modification d’instance qui affectent la classe hypothétique **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="186b4-125">The following example shows a query that requests notifications of all instance modification events that affect the hypothetical class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent
```



<span data-ttu-id="186b4-126">Si les événements associés à **EmailEvent** se produisent fréquemment, le consommateur est submergé d’événements.</span><span class="sxs-lookup"><span data-stu-id="186b4-126">If events associated with **EmailEvent** occur frequently, the consumer is flooded with events.</span></span> <span data-ttu-id="186b4-127">Une meilleure requête demande des événements uniquement lorsque des conditions spécifiques utilisent des propriétés de la classe spécifiée, par exemple lorsque le niveau d’importance est élevé.</span><span class="sxs-lookup"><span data-stu-id="186b4-127">A better query requests events only when specific conditions use properties of the class specified, such as when the importance level is high.</span></span>

<span data-ttu-id="186b4-128">L’exemple suivant illustre la requête que vous pouvez utiliser si **EmailImportance** est une propriété de la classe **EmailEvent**.</span><span class="sxs-lookup"><span data-stu-id="186b4-128">The following example shows the query you can use if **EmailImportance** is a property of the class **EmailEvent**.</span></span>


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



<span data-ttu-id="186b4-129">Notez que WMI peut rejeter une requête pour plusieurs raisons.</span><span class="sxs-lookup"><span data-stu-id="186b4-129">Note that WMI can reject a query for a number of reasons.</span></span> <span data-ttu-id="186b4-130">Par exemple, la requête peut être trop complexe ou gourmande en ressources pour l’évaluation.</span><span class="sxs-lookup"><span data-stu-id="186b4-130">For example, the query can be too complex or resource-intensive for evaluation.</span></span> <span data-ttu-id="186b4-131">Dans ce cas, WMI retourne des codes d’erreur spécifiques, tels que la **\_ requête WBEM E \_ non valide \_**.</span><span class="sxs-lookup"><span data-stu-id="186b4-131">When this occurs, WMI returns specific error codes, such as **WBEM\_E\_INVALID\_QUERY**.</span></span>

<span data-ttu-id="186b4-132">Les propriétés des objets incorporés peuvent être utilisées dans la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="186b4-132">Properties of embedded objects can be used in the WHERE clause.</span></span>

<span data-ttu-id="186b4-133">L’exemple suivant montre comment interroger des objets où la propriété **TargetInstance** de la classe système [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) est un objet [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incorporé et **FreeSpace** est une propriété du **\_ disque logique Win32**.</span><span class="sxs-lookup"><span data-stu-id="186b4-133">The following example shows how to query for objects where the **TargetInstance** property of the [**\_\_InstanceModificationEvent**](--instancemodificationevent.md) system class is an embedded [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) object and **FreeSpace** is a property of **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a><span data-ttu-id="186b4-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="186b4-134">Examples</span></span>

<span data-ttu-id="186b4-135">L’exemple d' [événement de création d’analyse pour un nom de processus spécifique](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sur TechNet utilise l’instruction SELECT pour surveiller les événements de création d’instance WMI pour \_ le processus Win32, en filtrant un nom de processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="186b4-135">The [Monitor creation event for specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sample on TechNet uses the SELECT statement to monitor WMI instance creation events for Win32\_Process, filtering for a specific process name.</span></span>

 

 
