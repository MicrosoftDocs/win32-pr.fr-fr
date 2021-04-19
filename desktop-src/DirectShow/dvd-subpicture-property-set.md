---
description: Les propriétés de sous-image de DVD contrôlent la couleur, le contraste et la sortie de l’affichage de la sous-image.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Jeu de propriétés de sous-image de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542416"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="fb745-103">Jeu de propriétés de sous-image de DVD</span><span class="sxs-lookup"><span data-stu-id="fb745-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="fb745-104">Les propriétés de sous-image de DVD contrôlent la couleur, le contraste et la sortie de l’affichage de la sous-image.</span><span class="sxs-lookup"><span data-stu-id="fb745-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="fb745-105">Les informations suivantes présentent les constantes et types de données nécessaires à utiliser pour ce jeu de propriétés dans les appels aux méthodes [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="fb745-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="fb745-106">Il fournit des valeurs pour les paramètres **GUID** (*GUIDPROPSET*), ID de propriété (*dwPropID*) et type de données de propriété (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="fb745-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="fb745-107">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="fb745-107">Property Set GUID</span></span> | <span data-ttu-id="fb745-108">AM \_ KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="fb745-108">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="fb745-109">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="fb745-109">Property ID</span></span>                           | <span data-ttu-id="fb745-110">Description</span><span class="sxs-lookup"><span data-stu-id="fb745-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb745-111">la \_ \_ composition DVDSUBPIC de la propriété am \_ \_ sur</span><span class="sxs-lookup"><span data-stu-id="fb745-111">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="fb745-112">Propriété définie uniquement qui active ou désactive l’affichage de sous-image.</span><span class="sxs-lookup"><span data-stu-id="fb745-112">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="fb745-113">DirectShow définit la **\_ \_ composition \_ de propriété AM sur** le type de données booléen pour cette propriété, ainsi que la \_ \_ composition de propriété PAM \_ sur en tant que pointeur vers ce type de données.</span><span class="sxs-lookup"><span data-stu-id="fb745-113">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="fb745-114">**True** indique que afficher la sous-image, **false** indique la désactiver.</span><span class="sxs-lookup"><span data-stu-id="fb745-114">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="fb745-115">Pour plus d’informations, consultez la partie WDM du DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fb745-115">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="fb745-116">AM, \_ propriété \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="fb745-116">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="fb745-117">Propriété définie uniquement qui spécifie un rectangle de sous-image ou d’écran dont la couleur ou le contraste seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="fb745-117">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="fb745-118">Le type de données est la [**\_ propriété am \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="fb745-118">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="fb745-119">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fb745-119">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="fb745-120">\_DVDSUBPIC, propriété, \_ \_ palette</span><span class="sxs-lookup"><span data-stu-id="fb745-120">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="fb745-121">Définit la palette pour une sous-image.</span><span class="sxs-lookup"><span data-stu-id="fb745-121">Sets the palette for a subpicture.</span></span> <span data-ttu-id="fb745-122">Le type de données est la [**\_ propriété am \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="fb745-122">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="fb745-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fb745-123">Remarks</span></span>

<span data-ttu-id="fb745-124">La **propriété \_ \_ DVDSUBPIC \_ HLI** est définie sur la propriété am uniquement.</span><span class="sxs-lookup"><span data-stu-id="fb745-124">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="fb745-125">Elle spécifie un rectangle de sous-image ou d’écran dont la couleur ou le contraste seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="fb745-125">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="fb745-126">Cela diffère de la spécification DVD-Video, dans le fait que le navigateur de DVD Microsoft analyse toutes les informations relatives aux boutons et au clavier et passe un seul rectangle de surbrillance au décodeur de sous-image à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="fb745-126">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="fb745-127">Par conséquent, les informations de mise en surbrillance sont envoyées au décodeur plus souvent qu’elles ne sont présentes dans le flux DVD.</span><span class="sxs-lookup"><span data-stu-id="fb745-127">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="fb745-128">Les informations de mise en surbrillance arrivent de manière asynchrone dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="fb745-128">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="fb745-129">Le décodeur utilise les horodatages de début et de fin de mise en surbrillance pour mettre en corrélation les informations de surbrillance avec les informations de sous-image pertinentes, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fb745-129">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="fb745-130">Si le décodeur n’a reçu aucune information de flux de sous-image pour les horodatages demandés, le décodeur suppose que les informations de mise en surbrillance sont autonomes et ne s’appliquent pas à une sous-image.</span><span class="sxs-lookup"><span data-stu-id="fb745-130">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="fb745-131">Dans ce cas, le décodeur suppose que les informations de couleur et de contraste sont toutes de la même couleur.</span><span class="sxs-lookup"><span data-stu-id="fb745-131">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="fb745-132">Les données ne sont pas entièrement au format de disque DVD.</span><span class="sxs-lookup"><span data-stu-id="fb745-132">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="fb745-133">Microsoft fournit une structure supplémentaire de type [**am \_ Property \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) qui est transmise en tant que paramètre à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="fb745-133">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="fb745-134">Cette structure décrit le bouton actuellement sélectionné à partir des informations de mise en surbrillance du DVD.</span><span class="sxs-lookup"><span data-stu-id="fb745-134">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="fb745-135">Le navigateur DVD traite toutes les informations de frappe et envoie de nouvelles informations de mise en surbrillance chaque fois qu’un état de bouton change.</span><span class="sxs-lookup"><span data-stu-id="fb745-135">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="fb745-136">Les informations décrivent un seul mode d’un bouton à la fois.</span><span class="sxs-lookup"><span data-stu-id="fb745-136">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="fb745-137">Il comprend un rectangle d’affichage en coordonnées de pixels de l’écran, ou un affichage de la sous-image, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="fb745-137">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="fb745-138">La structure contient également des informations de couleur et de contraste, mais uniquement pour l’état actuel du bouton actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fb745-138">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="fb745-139">Le format est défini dans la spécification du DVD.</span><span class="sxs-lookup"><span data-stu-id="fb745-139">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="fb745-140">Les informations de mise en surbrillance contiennent des horodatages de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="fb745-140">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="fb745-141">Celles-ci se trouvent dans les mêmes unités que d’autres horodatages, à deux exceptions près : un horodatage de début 0xFFFFFFFF signifie que la propriété de surbrillance est effective lors de la réception et un horodatage de fin 0xFFFFFFFF signifie que la propriété de surbrillance est valide jusqu’à la prochaine sélection reçue.</span><span class="sxs-lookup"><span data-stu-id="fb745-141">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="fb745-142">Le champ HLISS est défini dans la spécification du DVD.</span><span class="sxs-lookup"><span data-stu-id="fb745-142">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="fb745-143">La valeur zéro indique que toutes les mises en surbrillance ne sont pas valides et que le décodeur doit désactiver toutes les mises en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="fb745-143">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb745-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb745-144">Requirements</span></span>



| <span data-ttu-id="fb745-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb745-145">Requirement</span></span> | <span data-ttu-id="fb745-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb745-146">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb745-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb745-147">Header</span></span><br/> | <dl> <span data-ttu-id="fb745-148"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb745-148"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb745-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb745-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb745-150">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="fb745-150">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




