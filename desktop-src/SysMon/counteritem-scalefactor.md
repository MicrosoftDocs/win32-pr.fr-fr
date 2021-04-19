---
title: CounterItem. ScaleFactor, propriété
description: Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Propriété ScaleFactor SysMon
- Propriété ScaleFactor SysMon, classe CounterItem
- CounterItem classe SysMon, propriété ScaleFactor
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511568"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="e5e85-106">CounterItem. ScaleFactor, propriété</span><span class="sxs-lookup"><span data-stu-id="e5e85-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="e5e85-107">Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="e5e85-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="e5e85-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e5e85-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e85-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5e85-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="e5e85-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e5e85-110">Property value</span></span>

<span data-ttu-id="e5e85-111">Facteur d’échelle utilisé pour afficher les valeurs de compteur sous forme de graphique.</span><span class="sxs-lookup"><span data-stu-id="e5e85-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="e5e85-112">Les valeurs valides sont comprises entre-9 et 9 (les valeurs correspondent à 0,000000001-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="e5e85-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="e5e85-113">**Avant Windows Vista :** Les valeurs valides sont comprises entre-7 et 7 (les valeurs correspondent à 0,0000001-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="e5e85-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e85-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e5e85-114">Remarks</span></span>

<span data-ttu-id="e5e85-115">Définissez cette propriété uniquement si vous souhaitez modifier le facteur d’échelle par défaut du compteur (chaque compteur définit son propre facteur d’échelle).</span><span class="sxs-lookup"><span data-stu-id="e5e85-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="e5e85-116">La valeur de cette propriété est définie sur Integer. MaxValue si le compteur utilise son facteur d’échelle par défaut pour représenter les valeurs dans un graphique.</span><span class="sxs-lookup"><span data-stu-id="e5e85-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e85-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5e85-117">Requirements</span></span>



| <span data-ttu-id="e5e85-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5e85-118">Requirement</span></span> | <span data-ttu-id="e5e85-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5e85-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e85-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e85-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5e85-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e5e85-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5e85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e85-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5e85-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5e85-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e85-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e85-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e5e85-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e85-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5e85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e85-127">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="e5e85-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="e5e85-128">**SystemMonitor.ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="e5e85-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





