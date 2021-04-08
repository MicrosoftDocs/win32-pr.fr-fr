---
title: SystemMonitor. Highlight, propriété
description: Récupère ou définit une valeur indiquant si les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Mettre en surbrillance la propriété SysMon
- Mettre en surbrillance la propriété SysMon, classe SystemMonitor
- SystemMonitor classe SysMon, Highlight, propriété
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843617"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="73332-106">SystemMonitor. Highlight, propriété</span><span class="sxs-lookup"><span data-stu-id="73332-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="73332-107">Récupère ou définit une valeur indiquant si les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="73332-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="73332-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="73332-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73332-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73332-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="73332-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="73332-110">Property value</span></span>

<span data-ttu-id="73332-111">True indique que les valeurs des compteurs sélectionnés sont mises en surbrillance dans le graphique ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="73332-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="73332-112">La valeur par défaut est False.</span><span class="sxs-lookup"><span data-stu-id="73332-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="73332-113">Notes</span><span class="sxs-lookup"><span data-stu-id="73332-113">Remarks</span></span>

<span data-ttu-id="73332-114">Pour sélectionner un ou plusieurs compteurs, vous pouvez définir [**CounterItem. Selected**](counteritem-selected.md) sur true ou l’utilisateur peut sélectionner les compteurs dans la liste des compteurs affichée dans la légende.</span><span class="sxs-lookup"><span data-stu-id="73332-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="73332-115">**Avant Windows Vista :** Vous ne pouvez pas sélectionner des compteurs par programmation et l’utilisateur ne peut sélectionner qu’un seul compteur dans la liste des compteurs affichée dans la légende.</span><span class="sxs-lookup"><span data-stu-id="73332-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="73332-116">La mise en surbrillance peut être en noir ou en blanc, en fonction de la valeur de la propriété [**BackColor**](systemmonitor-backcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="73332-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="73332-117">La mise en surbrillance est automatiquement définie sur la couleur qui fournira un contraste suffisant entre la couleur de surbrillance et la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="73332-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="73332-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73332-118">Requirements</span></span>



| <span data-ttu-id="73332-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73332-119">Requirement</span></span> | <span data-ttu-id="73332-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="73332-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73332-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73332-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73332-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73332-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="73332-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73332-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73332-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73332-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73332-125">DLL</span><span class="sxs-lookup"><span data-stu-id="73332-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73332-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="73332-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73332-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73332-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73332-128">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="73332-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="73332-129">**CounterItem. Selected**</span><span class="sxs-lookup"><span data-stu-id="73332-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





