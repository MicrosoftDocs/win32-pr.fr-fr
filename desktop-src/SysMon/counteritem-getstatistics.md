---
title: Méthode CounterItem. GetStatistics
description: Récupère les valeurs moyennes, maximales et minimales du compteur.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Méthode GetStatistics SysMon
- Méthode GetStatistics SysMon, classe CounterItem
- CounterItem classe SysMon, méthode GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942256"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="a627b-106">Méthode CounterItem. GetStatistics</span><span class="sxs-lookup"><span data-stu-id="a627b-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="a627b-107">Récupère les valeurs moyennes, maximales et minimales du compteur.</span><span class="sxs-lookup"><span data-stu-id="a627b-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a627b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a627b-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="a627b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a627b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a627b-110">*maximum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a627b-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a627b-111">Valeur maximale du compteur.</span><span class="sxs-lookup"><span data-stu-id="a627b-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a627b-112">*min* \[ . à\]</span><span class="sxs-lookup"><span data-stu-id="a627b-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a627b-113">Valeur minimale du compteur.</span><span class="sxs-lookup"><span data-stu-id="a627b-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a627b-114">*moyenne* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a627b-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a627b-115">Valeur moyenne du compteur.</span><span class="sxs-lookup"><span data-stu-id="a627b-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a627b-116">*État* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a627b-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a627b-117">Indique si les valeurs sont valides.</span><span class="sxs-lookup"><span data-stu-id="a627b-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="a627b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a627b-118">Value</span></span>                                                                                              | <span data-ttu-id="a627b-119">Signification</span><span class="sxs-lookup"><span data-stu-id="a627b-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="a627b-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a627b-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a627b-121">Les valeurs sont valides.</span><span class="sxs-lookup"><span data-stu-id="a627b-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="a627b-122"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="a627b-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="a627b-123">Les valeurs ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a627b-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a627b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a627b-124">Return value</span></span>

<span data-ttu-id="a627b-125">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a627b-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a627b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a627b-126">Remarks</span></span>

<span data-ttu-id="a627b-127">Seules les valeurs de compteur qui sont visibles dans la fenêtre graphique sont utilisées pour calculer les valeurs statistiques.</span><span class="sxs-lookup"><span data-stu-id="a627b-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a627b-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a627b-128">Requirements</span></span>



| <span data-ttu-id="a627b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a627b-129">Requirement</span></span> | <span data-ttu-id="a627b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a627b-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a627b-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a627b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a627b-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a627b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a627b-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a627b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a627b-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a627b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a627b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a627b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a627b-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a627b-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a627b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a627b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a627b-138">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="a627b-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="a627b-139">**CounterItem.GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="a627b-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="a627b-140">**CounterItem. GetValue**</span><span class="sxs-lookup"><span data-stu-id="a627b-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





