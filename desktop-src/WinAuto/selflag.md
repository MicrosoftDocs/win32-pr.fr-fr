---
title: SELFLAG, constantes (oleacc. h)
description: Cette rubrique décrit les valeurs constantes utilisées pour spécifier la façon dont un objet accessible est sélectionné ou qui prend le focus.
ms.assetid: 52755540-dcf4-4e0b-bb5c-88b05f134d79
topic_type:
- apiref
api_name:
- SELFLAG_NONE
- SELFLAG_TAKEFOCUS
- SELFLAG_TAKESELECTION
- SELFLAG_EXTENDSELECTION
- SELFLAG_ADDSELECTION
- SELFLAG_REMOVESELECTION
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb49daffd2bb20e705d17aa51c3bff3d9622a6de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540442"
---
# <a name="selflag-constants"></a><span data-ttu-id="c3dcb-103">Constantes SELFLAG</span><span class="sxs-lookup"><span data-stu-id="c3dcb-103">SELFLAG Constants</span></span>

<span data-ttu-id="c3dcb-104">Cette rubrique décrit les valeurs constantes utilisées pour spécifier la façon dont un objet accessible est sélectionné ou qui prend le focus.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-104">This topic describes the constant values used to specify how an accessible object becomes selected or takes the focus.</span></span> <span data-ttu-id="c3dcb-105">Les constantes sont définies dans oleacc. h et sont utilisées avec la méthode [**IAccessible :: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) .</span><span class="sxs-lookup"><span data-stu-id="c3dcb-105">The constants are defined in oleacc.h and are used with the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method.</span></span>

<span data-ttu-id="c3dcb-106">Les combinaisons suivantes ne sont pas autorisées :</span><span class="sxs-lookup"><span data-stu-id="c3dcb-106">The following combinations are not allowed:</span></span>

-   <span data-ttu-id="c3dcb-107">SELFLAG \_ ADDSELECTION \| SELFLAG \_ REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-107">SELFLAG\_ADDSELECTION \| SELFLAG\_REMOVESELECTION</span></span>
-   <span data-ttu-id="c3dcb-108">SELFLAG \_ ADDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-108">SELFLAG\_ADDSELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="c3dcb-109">SELFLAG \_ REMOVESELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-109">SELFLAG\_REMOVESELECTION \| SELFLAG\_TAKESELECTION</span></span>
-   <span data-ttu-id="c3dcb-110">SELFLAG \_ EXTENDSELECTION \| SELFLAG \_ TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-110">SELFLAG\_EXTENDSELECTION \| SELFLAG\_TAKESELECTION</span></span>

<span data-ttu-id="c3dcb-111">**Remarque pour les clients :** Microsoft Active Accessibility ne prend pas en charge la sélection du texte contenu dans les contrôles Edit et Rich Edit, car le texte est exposé sous la forme d’une chaîne dans la [propriété Value](value-property.md)de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-111">**Note to clients :** Microsoft Active Accessibility does not support the selection of the text contained in edit and rich edit controls because the text is exposed as a string in the object's [Value property](value-property.md).</span></span>

<span data-ttu-id="c3dcb-112">Pour plus d’informations sur la façon d’effectuer des opérations de sélection complexes, consultez [sélection des objets enfants](selecting-child-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c3dcb-112">For information on how to perform complex selection operations, see [Selecting Child Objects](selecting-child-objects.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c3dcb-113">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="c3dcb-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c3dcb-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3dcb-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_NONE"></span><span id="selflag_none"></span><dl> <span data-ttu-id="c3dcb-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-115"><dt><strong>SELFLAG_NONE</strong></dt> <dt>0</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-116">N’effectue aucune action.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-116">Performs no action.</span></span> <span data-ttu-id="c3dcb-117">Microsoft Active Accessibility ne modifie pas la sélection ou le focus.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-117">Microsoft Active Accessibility does not change the selection or focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_TAKEFOCUS"></span><span id="selflag_takefocus"></span><dl> <span data-ttu-id="c3dcb-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-118"><dt><strong>SELFLAG_TAKEFOCUS</strong></dt> <dt>0x1</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-119">Définit le focus sur l’objet et en fait l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-119">Sets the focus to the object and makes it the selection anchor.</span></span> <span data-ttu-id="c3dcb-120">Utilisé par lui-même, cet indicateur ne modifie pas la sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-120">Used by itself, this flag does not alter the selection.</span></span> <span data-ttu-id="c3dcb-121">L’effet est similaire au déplacement manuel du focus en appuyant sur une touche de direction tout en maintenant la touche CTRL enfoncée dans l’Explorateur Windows ou dans une zone de liste à sélection multiple.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-121">The effect is similar to moving the focus manually by pressing an ARROW key while holding down the CTRL key in Windows Explorer or in any multiple-selection list box.</span></span> <br/> <span data-ttu-id="c3dcb-122">Avec les objets qui ont le <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS est combiné aux valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3dcb-122">With objects that have the <a href="object-state-constants.md"><strong>STATE_SYSTEM_MULTISELECTABLE</strong></a>, SELFLAG_TAKEFOCUS is combined with the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="c3dcb-123">SELFLAG_TAKESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-123">SELFLAG_TAKESELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-124">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-124">SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-125">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-125">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-126">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-126">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-127">SELFLAG_ADDSELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-128">SELFLAG_REMOVESELECTION | SELFLAG_EXTENDSELECTION</span></span></li>
</ul>
<span data-ttu-id="c3dcb-129">Si vous appelez <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible :: accSelect</strong></a> avec l’indicateur SELFLAG_TAKEFOCUS sur un objet qui a un <strong>HWND</strong>, l’indicateur prend effet uniquement si le parent de l’objet a déjà le focus.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-129">If you call <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect"><strong>IAccessible::accSelect</strong></a> with the SELFLAG_TAKEFOCUS flag on an object that has an <strong>HWND</strong>, the flag will take effect only if the object's parent already has the focus.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_TAKESELECTION"></span><span id="selflag_takeselection"></span><dl> <span data-ttu-id="c3dcb-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0X2</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-130"><dt><strong>SELFLAG_TAKESELECTION</strong></dt> <dt>0x2</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-131">Sélectionne l’objet et supprime la sélection de tous les autres objets dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-131">Selects the object and removes the selection from all other objects in the container.</span></span> <br/> <span data-ttu-id="c3dcb-132">À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-132">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="c3dcb-133">Le SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combinaison équivaut à un simple clic sur un élément dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-133">The SELFLAG_TAKESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to single-clicking an item in Windows Explorer.</span></span><br/> <span data-ttu-id="c3dcb-134">Cet indicateur ne doit pas être combiné avec les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="c3dcb-134">This flag must not be combined with the following flags:</span></span><br/>
<ul>
<li><span data-ttu-id="c3dcb-135">SELFLAG_ADDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-135">SELFLAG_ADDSELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-136">SELFLAG_REMOVESELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-136">SELFLAG_REMOVESELECTION</span></span></li>
<li><span data-ttu-id="c3dcb-137">SELFLAG_EXTENDSELECTION</span><span class="sxs-lookup"><span data-stu-id="c3dcb-137">SELFLAG_EXTENDSELECTION</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_EXTENDSELECTION"></span><span id="selflag_extendselection"></span><dl> <span data-ttu-id="c3dcb-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-138"><dt><strong>SELFLAG_EXTENDSELECTION</strong></dt> <dt>0x4</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-139">Modifie la sélection afin que tous les objets entre l’ancre de sélection et cet objet prennent l’état de sélection de l’objet d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-139">Alters the selection so that all objects between the selection anchor and this object take on the anchor object's selection state.</span></span> <span data-ttu-id="c3dcb-140">Si l'objet d'ancrage n'est pas sélectionné, les objets sont enlevés de la sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-140">If the anchor object is not selected, the objects are removed from the selection.</span></span> <span data-ttu-id="c3dcb-141">Si l’objet d’ancrage est sélectionné, la sélection est étendue pour inclure cet objet et tous les objets compris entre.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-141">If the anchor object is selected, the selection is extended to include this object and all the objects in between.</span></span> <span data-ttu-id="c3dcb-142">Définissez l’état de sélection en combinant cet indicateur avec SELFLAG_ADDSELECTION ou SELFLAG_REMOVESELECTION.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-142">Set the selection state by combining this flag with SELFLAG_ADDSELECTION or SELFLAG_REMOVESELECTION.</span></span> <br/> <span data-ttu-id="c3dcb-143">À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-143">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="c3dcb-144">Le SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combinaison revient à ajouter un élément à une sélection manuellement en maintenant la touche Maj enfoncée et en cliquant sur un objet non sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-144">The SELFLAG_EXTENDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the SHIFT key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="c3dcb-145">Cet indicateur n’est pas combiné avec SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-145">This flag is not combined with SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SELFLAG_ADDSELECTION"></span><span id="selflag_addselection"></span><dl> <span data-ttu-id="c3dcb-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-146"><dt><strong>SELFLAG_ADDSELECTION</strong></dt> <dt>0x8</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-147">Ajoute l’objet à la sélection actuelle ; le résultat possible est une sélection non contiguë.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-147">Adds the object to the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="c3dcb-148">À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-148">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="c3dcb-149">Le SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combinaison revient à ajouter un élément à une sélection manuellement en maintenant la touche CTRL enfoncée et en cliquant sur un objet non sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-149">The SELFLAG_ADDSELECTION | SELFLAG_TAKEFOCUS combination is equivalent to adding an item to a selection manually by holding down the CTRL key and clicking an unselected object in Windows Explorer.</span></span><br/> <span data-ttu-id="c3dcb-150">Cet indicateur n’est pas combiné avec SELFLAG_REMOVESELECTION ou SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-150">This flag is not combined with SELFLAG_REMOVESELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SELFLAG_REMOVESELECTION"></span><span id="selflag_removeselection"></span><dl> <span data-ttu-id="c3dcb-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span><span class="sxs-lookup"><span data-stu-id="c3dcb-151"><dt><strong>SELFLAG_REMOVESELECTION</strong></dt> <dt>0x10</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c3dcb-152">Supprime l’objet de la sélection actuelle ; le résultat possible est une sélection non contiguë.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-152">Removes the object from the current selection; possible result is a noncontiguous selection.</span></span> <br/> <span data-ttu-id="c3dcb-153">À moins qu’elle ne soit combinée avec SELFLAG_TAKEFOCUS, cet indicateur ne change pas le focus ou l’ancre de sélection.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-153">Unless it is combined with SELFLAG_TAKEFOCUS, this flag does not change the focus or the selection anchor.</span></span> <span data-ttu-id="c3dcb-154">Le SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combinaison équivaut à supprimer un élément d’une sélection manuellement, en maintenant la touche CTRL enfoncée tout en cliquant sur un objet sélectionné dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-154">The SELFLAG_REMOVESELECTION | SELFLAG_TAKEFOCUS combination is equivalent to removing an item from a selection manually, by holding down the CTRL key while clicking a selected object in Windows Explorer.</span></span><br/> <span data-ttu-id="c3dcb-155">Cet indicateur n’est pas combiné avec SELFLAG_ADDSELECTION ou SELFLAG_TAKESELECTION.</span><span class="sxs-lookup"><span data-stu-id="c3dcb-155">This flag is not combined with SELFLAG_ADDSELECTION or SELFLAG_TAKESELECTION.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c3dcb-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3dcb-156">Requirements</span></span>



| <span data-ttu-id="c3dcb-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3dcb-157">Requirement</span></span> | <span data-ttu-id="c3dcb-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3dcb-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dcb-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3dcb-159">Header</span></span><br/> | <dl> <span data-ttu-id="c3dcb-160"><dt>Oleacc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3dcb-160"><dt>Oleacc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3dcb-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3dcb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3dcb-162">**IAccessible :: accSelect**</span><span class="sxs-lookup"><span data-stu-id="c3dcb-162">**IAccessible::accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)
</dt> <dt>

[<span data-ttu-id="c3dcb-163">Sélection des objets enfants</span><span class="sxs-lookup"><span data-stu-id="c3dcb-163">Selecting Child Objects</span></span>](selecting-child-objects.md)
</dt> </dl>

 

 





