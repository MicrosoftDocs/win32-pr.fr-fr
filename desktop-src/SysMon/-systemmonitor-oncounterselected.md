---
title: Événement SystemMonitor. OnCounterSelected
description: Vous avertit lorsqu’un compteur est sélectionné.
ms.assetid: 788a95a7-47ec-41f9-bf46-324ad3cc8a4e
keywords:
- Événement OnCounterSelected SysMon
- Événement OnCounterSelected SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, événement OnCounterSelected
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterSelected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0174ab2f896a27e44df592ec28b7cb12a03198f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512165"
---
# <a name="systemmonitoroncounterselected-event"></a><span data-ttu-id="21e6a-106">Événement SystemMonitor. OnCounterSelected</span><span class="sxs-lookup"><span data-stu-id="21e6a-106">SystemMonitor.OnCounterSelected event</span></span>

<span data-ttu-id="21e6a-107">Vous avertit lorsqu’un compteur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="21e6a-107">Notifies you when a counter is selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e6a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21e6a-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterSelected( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="21e6a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21e6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e6a-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="21e6a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e6a-111">Index du compteur sélectionné dans l’objet de collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="21e6a-111">Index of the selected counter in the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e6a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21e6a-112">Return value</span></span>

<span data-ttu-id="21e6a-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="21e6a-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e6a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="21e6a-114">Remarks</span></span>

<span data-ttu-id="21e6a-115">Vous pouvez recevoir cet événement lorsque</span><span class="sxs-lookup"><span data-stu-id="21e6a-115">You can receive this event when</span></span>

-   <span data-ttu-id="21e6a-116">Vous définissez [**CounterItem. Selected**](counteritem-selected.md) sur true</span><span class="sxs-lookup"><span data-stu-id="21e6a-116">You set [**CounterItem.Selected**](counteritem-selected.md) to True</span></span>
-   <span data-ttu-id="21e6a-117">L’utilisateur sélectionne un compteur dans la légende</span><span class="sxs-lookup"><span data-stu-id="21e6a-117">The user selects a counter in the Legend</span></span>
-   <span data-ttu-id="21e6a-118">L’utilisateur double-clique sur un compteur dans la légende</span><span class="sxs-lookup"><span data-stu-id="21e6a-118">The user double-clicks on a counter in the Legend</span></span>

## <a name="requirements"></a><span data-ttu-id="21e6a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21e6a-119">Requirements</span></span>



| <span data-ttu-id="21e6a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21e6a-120">Requirement</span></span> | <span data-ttu-id="21e6a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="21e6a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21e6a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21e6a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21e6a-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21e6a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="21e6a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21e6a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21e6a-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21e6a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21e6a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="21e6a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21e6a-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="21e6a-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e6a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21e6a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e6a-129">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="21e6a-129">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="21e6a-130">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="21e6a-130">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> </dl>

 

 





