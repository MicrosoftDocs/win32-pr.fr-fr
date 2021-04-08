---
title: Objet CounterItem (Isysmon. h)
description: Utilisez cette classe pour récupérer le chemin d’accès et la valeur d’un compteur et pour spécifier la couleur utilisée pour représenter le compteur. Pour récupérer cet objet, appelez compteurs. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- CounterItem, objet SysMon
- Description de l’objet CounterItem SysMon
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741916"
---
# <a name="counteritem-object"></a><span data-ttu-id="4f4f7-106">Objet CounterItem</span><span class="sxs-lookup"><span data-stu-id="4f4f7-106">CounterItem object</span></span>

<span data-ttu-id="4f4f7-107">Utilisez cette classe pour récupérer le chemin d’accès et la valeur d’un compteur et pour spécifier la couleur utilisée pour représenter le compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="4f4f7-108">Pour récupérer cet objet, appelez [**compteurs. Item**](counters-item.md).</span><span class="sxs-lookup"><span data-stu-id="4f4f7-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="4f4f7-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4f4f7-109">Members</span></span>

<span data-ttu-id="4f4f7-110">L’objet **CounterItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f4f7-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="4f4f7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f4f7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4f4f7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f4f7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4f4f7-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f4f7-113">Methods</span></span>

<span data-ttu-id="4f4f7-114">L’objet **CounterItem** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="4f4f7-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4f4f7-115">Method</span></span>                                             | <span data-ttu-id="4f4f7-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f4f7-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="4f4f7-117">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="4f4f7-118">Récupère les données de compteur à partir d’un point spécifique dans le graphique linéaire.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="4f4f7-119">**GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="4f4f7-120">Récupère les valeurs moyennes, maximales et minimales du compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="4f4f7-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="4f4f7-122">Récupère la dernière valeur du compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="4f4f7-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4f4f7-123">Properties</span></span>

<span data-ttu-id="4f4f7-124">L’objet **CounterItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="4f4f7-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="4f4f7-125">Property</span></span>                                                  | <span data-ttu-id="4f4f7-126">Description</span><span class="sxs-lookup"><span data-stu-id="4f4f7-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="4f4f7-127">**Couleur**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="4f4f7-128">Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="4f4f7-129">**LineStyle**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="4f4f7-130">Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="4f4f7-131">**D**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="4f4f7-132">Récupère le chemin d’accès du compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="4f4f7-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="4f4f7-134">Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="4f4f7-135">**Sélectionné**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="4f4f7-136">Récupère ou définit une valeur qui indique si le compteur est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="4f4f7-137">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="4f4f7-138">Récupère la valeur actuelle du compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="4f4f7-139">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="4f4f7-140">Récupère ou définit une valeur qui indique si le compteur est graphique.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="4f4f7-141">**Width**</span><span class="sxs-lookup"><span data-stu-id="4f4f7-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="4f4f7-142">Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="4f4f7-143">Notes</span><span class="sxs-lookup"><span data-stu-id="4f4f7-143">Remarks</span></span>

<span data-ttu-id="4f4f7-144">La [**valeur**](counteritem-value.md) est la propriété par défaut de **CounterItem**.</span><span class="sxs-lookup"><span data-stu-id="4f4f7-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4f7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f4f7-145">Requirements</span></span>



| <span data-ttu-id="4f4f7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f4f7-146">Requirement</span></span> | <span data-ttu-id="4f4f7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f4f7-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4f7-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4f7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4f7-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f4f7-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4f4f7-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f4f7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4f7-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f4f7-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f4f7-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f4f7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f4f7-153"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4f7-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="4f4f7-154">DLL</span><span class="sxs-lookup"><span data-stu-id="4f4f7-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4f7-155"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="4f4f7-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4f7-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f4f7-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4f7-157">Classes SYSMON</span><span class="sxs-lookup"><span data-stu-id="4f4f7-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





