---
title: Compteurs. Remove, méthode
description: Supprime une instance CounterItem de la collection.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Supprimer la méthode SysMon
- Remove, méthode SysMon, classe Counters
- Compteurs Class SysMon, Remove, méthode
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941997"
---
# <a name="countersremove-method"></a><span data-ttu-id="3b0f6-106">Compteurs. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="3b0f6-106">Counters.Remove method</span></span>

<span data-ttu-id="3b0f6-107">Supprime une instance [**CounterItem**](counteritem.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b0f6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b0f6-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="3b0f6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b0f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b0f6-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b0f6-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b0f6-111">Index de l’objet [**CounterItem**](counteritem.md) à supprimer de la collection.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="3b0f6-112">L’index est de base un.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b0f6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b0f6-113">Return value</span></span>

<span data-ttu-id="3b0f6-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="3b0f6-115">Exceptions</span><span class="sxs-lookup"><span data-stu-id="3b0f6-115">Exceptions</span></span>



| <span data-ttu-id="3b0f6-116">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="3b0f6-116">Exception type</span></span>                                  | <span data-ttu-id="3b0f6-117">Condition</span><span class="sxs-lookup"><span data-stu-id="3b0f6-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3b0f6-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="3b0f6-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="3b0f6-119">L’index spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-119">The specified index is not valid.</span></span> <span data-ttu-id="3b0f6-120">La valeur de Err. Number est ???.</span><span class="sxs-lookup"><span data-stu-id="3b0f6-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3b0f6-121">Notes</span><span class="sxs-lookup"><span data-stu-id="3b0f6-121">Remarks</span></span>

<span data-ttu-id="3b0f6-122">Pour supprimer tous les compteurs de la collection, vous pouvez appeler [**systemmonitor. Reset**](systemmonitor-reset.md).</span><span class="sxs-lookup"><span data-stu-id="3b0f6-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b0f6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b0f6-123">Requirements</span></span>



| <span data-ttu-id="3b0f6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b0f6-124">Requirement</span></span> | <span data-ttu-id="3b0f6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b0f6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b0f6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b0f6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0f6-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b0f6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="3b0f6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b0f6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0f6-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b0f6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b0f6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3b0f6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b0f6-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="3b0f6-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b0f6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b0f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0f6-133">**Counters**</span><span class="sxs-lookup"><span data-stu-id="3b0f6-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="3b0f6-134">**SystemMonitor. Reset**</span><span class="sxs-lookup"><span data-stu-id="3b0f6-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





