---
title: CounterItem. LineStyle, propriété
description: Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Propriété LineStyle SysMon
- Propriété LineStyle SysMon, classe CounterItem
- Classe CounterItem SysMon, propriété LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942089"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="4c4a7-106">CounterItem. LineStyle, propriété</span><span class="sxs-lookup"><span data-stu-id="4c4a7-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="4c4a7-107">Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="4c4a7-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4a7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c4a7-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="4c4a7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4c4a7-110">Property value</span></span>

<span data-ttu-id="4c4a7-111">Style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="4c4a7-112">Les valeurs correspondent aux constantes système répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="4c4a7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c4a7-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="4c4a7-114">Signification</span><span class="sxs-lookup"><span data-stu-id="4c4a7-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="4c4a7-115"><dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="4c4a7-116">Ligne pleine.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-116">Solid line.</span></span> <span data-ttu-id="4c4a7-117">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="4c4a7-118"><dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="4c4a7-119">Ligne en pointillés avec des segments longs et des espaces étroits.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="4c4a7-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="4c4a7-121">Ligne en pointillés avec des segments et des espaces uniformes.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="4c4a7-122"><dt>**System. Drawing. Drawing2D. DashStyle. tiret point**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="4c4a7-123">Ligne en pointillés avec des segments courts et longs.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="4c4a7-124"><dt>**System. Drawing. Drawing2D. DashStyle. tiret point point**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="4c4a7-125">Ligne en pointillés avec des tirets et des points doubles en alternance.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="4c4a7-126">Exceptions</span><span class="sxs-lookup"><span data-stu-id="4c4a7-126">Exceptions</span></span>



| <span data-ttu-id="4c4a7-127">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="4c4a7-127">Exception type</span></span>               | <span data-ttu-id="4c4a7-128">Condition</span><span class="sxs-lookup"><span data-stu-id="4c4a7-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="4c4a7-129">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="4c4a7-129">**System.ArgumentException**</span></span> | <span data-ttu-id="4c4a7-130">Le style de ligne spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4c4a7-131">Notes</span><span class="sxs-lookup"><span data-stu-id="4c4a7-131">Remarks</span></span>

<span data-ttu-id="4c4a7-132">Pour spécifier une valeur autre que DashStyle. Solid, [**CounterItem. Width**](counteritem-width.md) doit avoir la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="4c4a7-133">Si la largeur est supérieure à 1, SYSMON ignore le style de ligne spécifié et utilise DashStyle. Solid.</span><span class="sxs-lookup"><span data-stu-id="4c4a7-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4a7-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c4a7-134">Requirements</span></span>



| <span data-ttu-id="4c4a7-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c4a7-135">Requirement</span></span> | <span data-ttu-id="4c4a7-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c4a7-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4a7-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c4a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4a7-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c4a7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4c4a7-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c4a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4a7-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c4a7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c4a7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4c4a7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c4a7-142"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4c4a7-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4a7-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c4a7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4a7-144">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="4c4a7-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





