---
title: CounterItem. Color, propriété
description: Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Propriété de couleur SysMon
- Propriété Color SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété Color
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741917"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="f42df-106">CounterItem. Color, propriété</span><span class="sxs-lookup"><span data-stu-id="f42df-106">CounterItem.Color property</span></span>

<span data-ttu-id="f42df-107">Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="f42df-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="f42df-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f42df-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f42df-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f42df-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="f42df-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f42df-110">Property value</span></span>

<span data-ttu-id="f42df-111">Couleur utilisée pour représenter sous forme graphique la valeur du compteur.</span><span class="sxs-lookup"><span data-stu-id="f42df-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f42df-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f42df-112">Remarks</span></span>

<span data-ttu-id="f42df-113">Si vous ne spécifiez pas la couleur à utiliser, SYSMON sélectionne les couleurs des seize premiers compteurs.</span><span class="sxs-lookup"><span data-stu-id="f42df-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="f42df-114">Si vous spécifiez plus de seize compteurs, SYSMON utilise les mêmes couleurs des seize premiers compteurs.</span><span class="sxs-lookup"><span data-stu-id="f42df-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="f42df-115">Pour vous aider à distinguer les compteurs les uns des autres, SYSMON change le [**style de ligne**](counteritem-linestyle.md) utilisé pour chaque multiple de seize compteurs jusqu’aux 80 premiers compteurs.</span><span class="sxs-lookup"><span data-stu-id="f42df-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="f42df-116">Par exemple, les seize premiers compteurs utilisent un style de ligne plein, les seize suivants utilisent un style de ligne de tirets, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f42df-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="f42df-117">SYSMON définit ensuite la [**largeur de ligne**](counteritem-width.md) sur 2 pour les compteurs 81-96 et sur 3 pour les compteurs 96-112.</span><span class="sxs-lookup"><span data-stu-id="f42df-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="f42df-118">Si la collection contient plus de 112 compteurs, les compteurs contiendront des valeurs de couleur, de style de ligne et de largeur en double.</span><span class="sxs-lookup"><span data-stu-id="f42df-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="f42df-119">**Avant Windows Vista :** Si vous ne spécifiez pas la couleur à utiliser, SYSMON sélectionne les couleurs des seize premiers compteurs.</span><span class="sxs-lookup"><span data-stu-id="f42df-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="f42df-120">Si vous spécifiez plus de seize compteurs, SYSMON utilise les mêmes couleurs des seize premiers compteurs.</span><span class="sxs-lookup"><span data-stu-id="f42df-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="f42df-121">Pour mieux distinguer les compteurs les uns des autres, SYSMON augmente la [**largeur de ligne**](counteritem-width.md) des trois premiers compteurs qui reçoivent la même affectation de couleur.</span><span class="sxs-lookup"><span data-stu-id="f42df-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="f42df-122">Si plus de trois compteurs utilisent la même couleur, SYSMON choisit de façon aléatoire la largeur de ligne à utiliser pour le compteur.</span><span class="sxs-lookup"><span data-stu-id="f42df-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42df-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f42df-123">Requirements</span></span>



| <span data-ttu-id="f42df-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f42df-124">Requirement</span></span> | <span data-ttu-id="f42df-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f42df-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f42df-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f42df-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f42df-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f42df-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f42df-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f42df-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f42df-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f42df-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f42df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f42df-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f42df-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f42df-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42df-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f42df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f42df-133">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="f42df-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





