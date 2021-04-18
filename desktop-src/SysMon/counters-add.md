---
title: Counters. Add, méthode
description: Ajoute une instance CounterItem à la collection.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Ajouter la méthode SysMon
- Ajouter la méthode SysMon, classe Counters
- Compteurs classe SysMon, méthode Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c974c5df6f531cd75292290c61534a923e5be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464715"
---
# <a name="countersadd-method"></a><span data-ttu-id="b96c1-106">Counters. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="b96c1-106">Counters.Add method</span></span>

<span data-ttu-id="b96c1-107">Ajoute une instance [**CounterItem**](counteritem.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="b96c1-107">Adds a [**CounterItem**](counteritem.md) instance to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b96c1-108">Syntax</span></span>


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a><span data-ttu-id="b96c1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b96c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b96c1-110">*nom du chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b96c1-110">*pathname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b96c1-111">Chemin d’accès au compteur.</span><span class="sxs-lookup"><span data-stu-id="b96c1-111">Path to the counter.</span></span> <span data-ttu-id="b96c1-112">Le chemin d’accès peut inclure un nom d’ordinateur et doit inclure un nom d’objet de performance, un nom d’instance d’objet si l’objet de performance spécifié prend en charge plusieurs instances et un nom de compteur.</span><span class="sxs-lookup"><span data-stu-id="b96c1-112">The path can include a machine name, and must include a performance object name, an object instance name if the specified performance object supports multiple instances, and a counter name.</span></span> <span data-ttu-id="b96c1-113">Cette spécification de chemin d’accès ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="b96c1-113">This path specification is not case-sensitive.</span></span>

<span data-ttu-id="b96c1-114">Pour plus d’informations sur la spécification d’un chemin d’accès de compteur, consultez [spécification d’un chemin d’accès de compteur](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span><span class="sxs-lookup"><span data-stu-id="b96c1-114">For details on specifying a counter path, see [Specifying a Counter Path](/windows/desktop/PerfCtrs/specifying-a-counter-path).</span></span>

</dd> </dl>

## <a name="exceptions"></a><span data-ttu-id="b96c1-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="b96c1-115">Exceptions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b96c1-116">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="b96c1-116">Exception type</span></span></th>
<th><span data-ttu-id="b96c1-117">Condition</span><span class="sxs-lookup"><span data-stu-id="b96c1-117">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b96c1-118"><strong>System. Runtime. InteropServices. COMException</strong></span><span class="sxs-lookup"><span data-stu-id="b96c1-118"><strong>System.Runtime.InteropServices.COMException</strong></span></span></td>
<td><span data-ttu-id="b96c1-119">Vous pouvez recevoir cette exception pour l’une des raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="b96c1-119">You can receive this exception for one of the following reasons:</span></span>
<ul>
<li><span data-ttu-id="b96c1-120">L’objet de performance spécifié est introuvable sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b96c1-120">The specified performance object was not found on the computer.</span></span> <span data-ttu-id="b96c1-121">La valeur de Err. Number est 0xC0000BB8.</span><span class="sxs-lookup"><span data-stu-id="b96c1-121">The Err.Number value is 0xC0000BB8.</span></span></li>
<li><span data-ttu-id="b96c1-122">Le compteur spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b96c1-122">The specified counter could not be found.</span></span> <span data-ttu-id="b96c1-123">La valeur de Err. Number est 0xC0000BB9.</span><span class="sxs-lookup"><span data-stu-id="b96c1-123">The Err.Number value is 0xC0000BB9.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b96c1-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b96c1-124">Remarks</span></span>

<span data-ttu-id="b96c1-125">Si vous spécifiez un compteur de caractères génériques dans le paramètre *pathname* , la méthode **Add** crée un objet [**CounterItem**](counteritem.md) pour chaque chemin d’accès développé.</span><span class="sxs-lookup"><span data-stu-id="b96c1-125">If you specify a wildcard counter in the *pathname* parameter, the **Add** method creates one [**CounterItem**](counteritem.md) object for each expanded path.</span></span> <span data-ttu-id="b96c1-126">La méthode **Add** retourne ensuite un pointeur vers le premier **CounterItem** ajouté.</span><span class="sxs-lookup"><span data-stu-id="b96c1-126">The **Add** method then returns a pointer to the first added **CounterItem**.</span></span>

<span data-ttu-id="b96c1-127">Si le caractère générique se traduirait par un compteur dupliqué, l’erreur n’est pas signalée et aucun doublon n’est créé.</span><span class="sxs-lookup"><span data-stu-id="b96c1-127">If the wildcard would result in a duplicate counter, the error is not reported and no duplicate is created.</span></span> <span data-ttu-id="b96c1-128">Si une condition d’erreur se produit avant la création de tous les compteurs, l’erreur est signalée et les autres compteurs ne sont pas créés.</span><span class="sxs-lookup"><span data-stu-id="b96c1-128">If an error condition occurs before all counters are created, the error is reported and the remaining counters are not created.</span></span>

<span data-ttu-id="b96c1-129">Il n’existe aucune limite au nombre de compteurs que vous pouvez ajouter. Toutefois, SYSMON affiche uniquement les premiers compteurs 1 024 de la collection.</span><span class="sxs-lookup"><span data-stu-id="b96c1-129">There is no limit to the number of counters that you can add; however, SYSMON will graph only the first 1,024 counters in the collection.</span></span> <span data-ttu-id="b96c1-130">Il n’existe aucune limite quant au nombre de compteurs que SYSMON affiche dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="b96c1-130">There is no limit on the number of counters that SYSMON will display in a report.</span></span>

<span data-ttu-id="b96c1-131">Pour recevoir une notification lorsqu’un compteur est ajouté, implémentez l’événement [OnCounterAdded](systemmonitor-oncounteradded.md) .</span><span class="sxs-lookup"><span data-stu-id="b96c1-131">To receive notification when a counter is added, implement the [OnCounterAdded](systemmonitor-oncounteradded.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b96c1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b96c1-132">Requirements</span></span>



| <span data-ttu-id="b96c1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b96c1-133">Requirement</span></span> | <span data-ttu-id="b96c1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b96c1-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b96c1-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b96c1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b96c1-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b96c1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b96c1-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b96c1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b96c1-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b96c1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b96c1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b96c1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b96c1-140"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b96c1-140"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b96c1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b96c1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96c1-142">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="b96c1-142">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="b96c1-143">**Counters**</span><span class="sxs-lookup"><span data-stu-id="b96c1-143">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="b96c1-144">**SystemMonitor.BrowseCounters**</span><span class="sxs-lookup"><span data-stu-id="b96c1-144">**SystemMonitor.BrowseCounters**</span></span>](systemmonitor-browsecounters.md)
</dt> </dl>

 

