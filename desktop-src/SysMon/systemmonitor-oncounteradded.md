---
title: Événement SystemMonitor. OnCounterAdded
description: Vous avertit lorsqu’un compteur est ajouté à la collection de compteurs.
ms.assetid: f798443f-e2f1-4d25-b142-d88d6e4fe12c
keywords:
- Événement OnCounterAdded SysMon
- Événement OnCounterAdded SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, événement OnCounterAdded
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterAdded
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f150709114ae25da89b107c7de85e3c5eca2551f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509920"
---
# <a name="systemmonitoroncounteradded-event"></a><span data-ttu-id="87202-106">Événement SystemMonitor. OnCounterAdded</span><span class="sxs-lookup"><span data-stu-id="87202-106">SystemMonitor.OnCounterAdded event</span></span>

<span data-ttu-id="87202-107">Vous avertit lorsqu’un compteur est ajouté à la collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="87202-107">Notifies you when a counter is added to the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="87202-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87202-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterAdded( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="87202-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87202-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87202-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87202-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87202-111">Index du compteur ajouté à l’objet de collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="87202-111">Index of the counter added to the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87202-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87202-112">Return value</span></span>

<span data-ttu-id="87202-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="87202-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="87202-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87202-114">Requirements</span></span>



| <span data-ttu-id="87202-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87202-115">Requirement</span></span> | <span data-ttu-id="87202-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="87202-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87202-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87202-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87202-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87202-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="87202-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87202-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87202-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87202-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87202-121">DLL</span><span class="sxs-lookup"><span data-stu-id="87202-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87202-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="87202-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87202-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87202-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87202-124">**SystemMonitor.OnCounterDeleted**</span><span class="sxs-lookup"><span data-stu-id="87202-124">**SystemMonitor.OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
</dt> <dt>

[<span data-ttu-id="87202-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="87202-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





