---
title: CounterItem. Selected, propriété
description: Récupère ou définit une valeur qui indique si le compteur est sélectionné.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propriété sélectionnée SysMon
- Propriété sélectionnée SysMon, objet CounterItem
- CounterItem objet SysMon, propriété sélectionnée
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942231"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="5d128-106">CounterItem. Selected, propriété</span><span class="sxs-lookup"><span data-stu-id="5d128-106">CounterItem.Selected property</span></span>

<span data-ttu-id="5d128-107">Récupère ou définit une valeur qui indique si le compteur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="5d128-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="5d128-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5d128-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d128-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d128-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="5d128-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5d128-110">Property value</span></span>

<span data-ttu-id="5d128-111">True si le compteur est sélectionné ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="5d128-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d128-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5d128-112">Remarks</span></span>

<span data-ttu-id="5d128-113">Vous pouvez sélectionner un ou plusieurs compteurs dans la collection de compteurs.</span><span class="sxs-lookup"><span data-stu-id="5d128-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="5d128-114">En sélectionnant un compteur, sélectionne le compteur dans la légende, rend le compteur visible dans la légende et génère un événement [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .</span><span class="sxs-lookup"><span data-stu-id="5d128-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d128-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d128-115">Requirements</span></span>



| <span data-ttu-id="5d128-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d128-116">Requirement</span></span> | <span data-ttu-id="5d128-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d128-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d128-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d128-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d128-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d128-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d128-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d128-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d128-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d128-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d128-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5d128-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d128-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5d128-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d128-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d128-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d128-125">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="5d128-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





