---
description: Cette section décrit les indicateurs utilisés par les méthodes de l’interface IActiveDesktop.
title: Indicateurs IActiveDesktop (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982930"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="c4624-103">Indicateurs IActiveDesktop</span><span class="sxs-lookup"><span data-stu-id="c4624-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="c4624-104">Cette section décrit les indicateurs utilisés par les méthodes de l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="c4624-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="c4624-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ appliquer \_ tout**</span><span class="sxs-lookup"><span data-stu-id="c4624-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-106">Agrégat des valeurs \* \* \* \* AD \_ apply \_ Save \* \* \* \*, \* \* \* \* Active Directory Apply \_ \_ HTMLGEN \* \* \* \* et \* \* \* \* ad \_ apply \_ Refresh \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="c4624-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**actualisation de la \_ \_ mise en mémoire tampon appliquée par Active Directory \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-108">Démarre un minuteur et regroupe toutes les demandes d’actualisation effectuées avec cet indicateur au cours de cet intervalle de temps en une seule actualisation.</span><span class="sxs-lookup"><span data-stu-id="c4624-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="c4624-109">Cet intervalle est défini sur cinq secondes.</span><span class="sxs-lookup"><span data-stu-id="c4624-109">This interval is set at five seconds.</span></span> <span data-ttu-id="c4624-110">À la fin de l’intervalle, ou si une actualisation est demandée au cours de l’intervalle sans un indicateur \* \* \* \* AD \_ apply- \_ buffer \_ Refresh \* \* \* \*, l’actualisation est effectuée et le minuteur est arrêté.</span><span class="sxs-lookup"><span data-stu-id="c4624-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="c4624-111">Cet indicateur doit être combiné avec l’indicateur \* \* \* \* AD \_ apply \_ Refresh \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="c4624-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**application active AD \_ \_ DYNAMICREFRESH**</span><span class="sxs-lookup"><span data-stu-id="c4624-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-113">[Version 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="c4624-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="c4624-114">Utilisez le HTML dynamique pour actualiser uniquement les éléments qui ont été modifiés depuis la dernière actualisation, et non l’intégralité du bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_application \_ FORCÉe ad**</span><span class="sxs-lookup"><span data-stu-id="c4624-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-116">Forcer une modification active sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**application active AD \_ \_ HTMLGEN**</span><span class="sxs-lookup"><span data-stu-id="c4624-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-118">Régénérez le fichier HTML du bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**actualisation de l' \_ application ad \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-120">Actualisez l’élément du bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ appliquer \_ Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="c4624-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-122">Enregistrez l’élément du bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ tout**</span><span class="sxs-lookup"><span data-stu-id="c4624-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-124">Agrégat des valeurs de COMP \_ elem \_ \* .</span><span class="sxs-lookup"><span data-stu-id="c4624-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ elem \_ activé**</span><span class="sxs-lookup"><span data-stu-id="c4624-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-126">L’élément a été activé.</span><span class="sxs-lookup"><span data-stu-id="c4624-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ elem \_ CURITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="c4624-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-128">État actuel de l’élément de bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ elem \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="c4624-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-130">Nom convivial de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem- \_ Scroll elem**</span><span class="sxs-lookup"><span data-stu-id="c4624-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-132">L’élément ne peut pas faire l’objet d’un défilement.</span><span class="sxs-lookup"><span data-stu-id="c4624-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ . \_ CSI d’origine elem \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-134">Informations d’état de l’élément de bureau d’origine.</span><span class="sxs-lookup"><span data-stu-id="c4624-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ elem \_ CDE à \_ gauche**</span><span class="sxs-lookup"><span data-stu-id="c4624-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-136">Position horizontale de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ CDE POS \_ Top**</span><span class="sxs-lookup"><span data-stu-id="c4624-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-138">Position verticale de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ elem \_ CDE \_ ZINDEX**</span><span class="sxs-lookup"><span data-stu-id="c4624-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-140">Index z de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ - \_ CSI restauré**</span><span class="sxs-lookup"><span data-stu-id="c4624-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-142">Informations d’état de l’élément de bureau restaurées.</span><span class="sxs-lookup"><span data-stu-id="c4624-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**RESPECTER \_ la \_ hauteur de taille elem \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-144">Hauteur de l'élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**RESPECTER la largeur de la \_ \_ taille elem \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-146">Largeur de l'élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP \_ elem \_ source**</span><span class="sxs-lookup"><span data-stu-id="c4624-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-148">Source d’origine de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP \_ elem ( \_ type)**</span><span class="sxs-lookup"><span data-stu-id="c4624-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-150">Type d'élément.</span><span class="sxs-lookup"><span data-stu-id="c4624-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP \_ type \_ CFHTML**</span><span class="sxs-lookup"><span data-stu-id="c4624-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-152">Format HTML compressé.</span><span class="sxs-lookup"><span data-stu-id="c4624-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP ( \_ contrôle de type) \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-154">L’élément est un contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4624-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP \_ type \_ htmldoc**</span><span class="sxs-lookup"><span data-stu-id="c4624-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-156">L’élément est un document HTML.</span><span class="sxs-lookup"><span data-stu-id="c4624-156">The item is an HTML document.</span></span> <span data-ttu-id="c4624-157">Cet indicateur doit être utilisé uniquement lorsque cela est absolument nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c4624-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="c4624-158">Cela entraîne l’insertion textuelle d’un document HTML dans le fichier Desktop. htt utilisé pour contrôler la disposition du bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="c4624-159">Dans la plupart des cas, vous devez utiliser l’indicateur \* \* \* \* COMP \_ type \_ Web \* \* \* \* pour ajouter des éléments au bureau.</span><span class="sxs-lookup"><span data-stu-id="c4624-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**TYPE de COMP \_ \_ Max.**</span><span class="sxs-lookup"><span data-stu-id="c4624-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-161">Valeur maximale d’un indicateur de \_ type COMP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="c4624-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_image de type de comp \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-163">L’élément est une image.</span><span class="sxs-lookup"><span data-stu-id="c4624-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_site Web type de comp \_**</span><span class="sxs-lookup"><span data-stu-id="c4624-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-165">L’élément est un site Web.</span><span class="sxs-lookup"><span data-stu-id="c4624-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPOSANT en \_ haut**</span><span class="sxs-lookup"><span data-stu-id="c4624-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-167">Valeur d’ordre de plan qui signifie que l’élément est en haut.</span><span class="sxs-lookup"><span data-stu-id="c4624-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**\_Centre WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="c4624-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-169">Le papier peint est centré.</span><span class="sxs-lookup"><span data-stu-id="c4624-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**</span><span class="sxs-lookup"><span data-stu-id="c4624-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-171">Valeur maximale d’un indicateur WPSTYLE \_ \* .</span><span class="sxs-lookup"><span data-stu-id="c4624-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**</span><span class="sxs-lookup"><span data-stu-id="c4624-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-173">Le papier peint est étiré pour s’ajuster à la totalité de l’écran.</span><span class="sxs-lookup"><span data-stu-id="c4624-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_vignette WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="c4624-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-175">Le papier peint est disposé en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="c4624-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c4624-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_étendue WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="c4624-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c4624-177">**Windows 8 et versions ultérieures**: le papier peint s’étend sur plusieurs moniteurs.</span><span class="sxs-lookup"><span data-stu-id="c4624-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4624-178">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4624-178">Requirements</span></span>



| <span data-ttu-id="c4624-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4624-179">Requirement</span></span> | <span data-ttu-id="c4624-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4624-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4624-181">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4624-181">Header</span></span><br/> | <dl> <span data-ttu-id="c4624-182"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4624-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
