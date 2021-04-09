---
title: Événement SystemMonitor. OnCounterDeleted
description: Vous avertit avant qu’un compteur soit supprimé de la collection de compteurs.
ms.assetid: ab6bc1ba-20cd-4774-853e-b6adb765fae3
keywords:
- Événement OnCounterDeleted SysMon
- Événement OnCounterDeleted SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, événement OnCounterDeleted
topic_type:
- apiref
api_name:
- SystemMonitor.OnCounterDeleted
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceafcc73f38e5413e312d00bf8aa8eba4eaf2c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942181"
---
# <a name="systemmonitoroncounterdeleted-event"></a><span data-ttu-id="064be-106">Événement SystemMonitor. OnCounterDeleted</span><span class="sxs-lookup"><span data-stu-id="064be-106">SystemMonitor.OnCounterDeleted event</span></span>

<span data-ttu-id="064be-107">Vous avertit avant qu’un compteur soit supprimé de la collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="064be-107">Notifies you before a counter is deleted from the [**Counters**](counters.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="064be-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="064be-108">Syntax</span></span>


```VB
SystemMonitor.OnCounterDeleted( _
  ByVal index As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="064be-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="064be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="064be-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="064be-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="064be-111">Index du compteur à supprimer de l’objet de collection de [**compteurs**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="064be-111">Index of the counter to be deleted from the [**Counters**](counters.md) collection object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="064be-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="064be-112">Return value</span></span>

<span data-ttu-id="064be-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="064be-113">This event does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="064be-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="064be-114">Requirements</span></span>



| <span data-ttu-id="064be-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="064be-115">Requirement</span></span> | <span data-ttu-id="064be-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="064be-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="064be-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="064be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="064be-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="064be-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="064be-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="064be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="064be-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="064be-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="064be-121">DLL</span><span class="sxs-lookup"><span data-stu-id="064be-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="064be-122"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="064be-122"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="064be-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="064be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="064be-124">**SystemMonitor.OnCounterAdded**</span><span class="sxs-lookup"><span data-stu-id="064be-124">**SystemMonitor.OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
</dt> <dt>

[<span data-ttu-id="064be-125">**SystemMonitor.OnCounterSelected**</span><span class="sxs-lookup"><span data-stu-id="064be-125">**SystemMonitor.OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
</dt> </dl>

 

 





