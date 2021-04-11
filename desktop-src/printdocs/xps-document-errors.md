---
description: Le tableau suivant répertorie toutes les valeurs HRESULT qui peuvent être retournées par les méthodes de l’API de document XPS.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: Erreurs de document XPS (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202243"
---
# <a name="xps-document-errors"></a><span data-ttu-id="a524a-103">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="a524a-103">XPS Document Errors</span></span>

<span data-ttu-id="a524a-104">Le tableau suivant répertorie toutes les valeurs **HRESULT** qui peuvent être retournées par les méthodes de l’API de document XPS.</span><span class="sxs-lookup"><span data-stu-id="a524a-104">The following table lists all the **HRESULT** values that can be returned by the methods of the XPS Document API.</span></span> <span data-ttu-id="a524a-105">Notez que toutes les méthodes ne retournent pas toutes les valeurs de retour listées dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="a524a-105">Note that not every method returns every return value that is listed in this table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a524a-106">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a524a-106">Return code/value</span></span></th>
<th><span data-ttu-id="a524a-107">Description</span><span class="sxs-lookup"><span data-stu-id="a524a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <span data-ttu-id="a524a-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-109">L’interface a déjà un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="a524a-109">The interface already has an owner.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <span data-ttu-id="a524a-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-111">Les dimensions de la zone de fond perdu ne sont pas compatibles avec les dimensions de page.</span><span class="sxs-lookup"><span data-stu-id="a524a-111">The bleed box dimensions are not compatible with the page dimensions.</span></span><br/> <span data-ttu-id="a524a-112">La largeur de la zone de fond perdu doit être supérieure ou égale à la largeur de page plus la valeur absolue de la coordonnée x de l’origine de la zone de fond perdu.</span><span class="sxs-lookup"><span data-stu-id="a524a-112">The bleed box width value must be greater than or equal to the page width plus the absolute value of the x-coordinate of the bleed box origin.</span></span> <span data-ttu-id="a524a-113">La valeur de la hauteur de la zone de fond perdu doit être supérieure ou égale à la hauteur de page plus la valeur absolue de la coordonnée y de l’origine de la zone de fond perdu.</span><span class="sxs-lookup"><span data-stu-id="a524a-113">The bleed box height value must be greater than or equal to the page height plus the absolute value of the y-coordinate of the bleed box origin.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <span data-ttu-id="a524a-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-115">Un élément <strong>PathGeometry</strong> contient un ensemble de chiffres de tracés spécifiés avec l’attribut <strong>figures</strong> ou avec un élément <strong>PathFigure</strong> enfant.</span><span class="sxs-lookup"><span data-stu-id="a524a-115">A <strong>PathGeometry</strong> element contains a set of path figures that are specified either with the <strong>Figures</strong> attribute or with a child <strong>PathFigure</strong> element.</span></span> <span data-ttu-id="a524a-116">Les figures de tracé d’une géométrie ne peuvent pas avoir à la fois l’attribut <strong>figures</strong> et un élément <strong>PathFigure</strong> enfant.</span><span class="sxs-lookup"><span data-stu-id="a524a-116">The path figures of a geometry cannot have both the <strong>Figures</strong> attribute and a child <strong>PathFigure</strong> element.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <span data-ttu-id="a524a-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-118">Un élément <strong>ResourceDictionary</strong> qui spécifie un dictionnaire de ressources distant dans son attribut <strong>source</strong> ne doit pas contenir d’enfants de définition de ressource.</span><span class="sxs-lookup"><span data-stu-id="a524a-118">A <strong>ResourceDictionary</strong> element that specifies a remote resource dictionary in its <strong>Source</strong> attribute MUST NOT contain any resource definition children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <span data-ttu-id="a524a-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-120">Une valeur d’emplacement du signe insertion n’est pas dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="a524a-120">A caret location value is out of order.</span></span> <span data-ttu-id="a524a-121">Les valeurs d’emplacement doivent être triées dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="a524a-121">The location values must be sorted in ascending order.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <span data-ttu-id="a524a-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-123">Des arrêts de signe insertion ont été spécifiés pour une chaîne vide ; ou bien, l’index de saut du signe insertion a dépassé la longueur de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-123">Caret stops were specified for an empty string; or, the caret jump index has exceeded the length of the Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <span data-ttu-id="a524a-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-125">Une valeur de couleur est hors limites.</span><span class="sxs-lookup"><span data-stu-id="a524a-125">A color value is out of range.</span></span><br/> <span data-ttu-id="a524a-126">Pour <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> types de couleurs, la valeur du canal alpha doit être supérieure ou égale à 0,0 et inférieure ou égale à + 1,0.</span><span class="sxs-lookup"><span data-stu-id="a524a-126">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> color types, the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span><br/> <span data-ttu-id="a524a-127">Pour <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> types de couleurs, <strong>channelValues [0]</strong> qui représente la valeur du canal alpha doit être supérieur ou égal à 0,0 et inférieur ou égal à + 1,0.</span><span class="sxs-lookup"><span data-stu-id="a524a-127">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> color types, the <strong>channelValues[0]</strong> that represents the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <span data-ttu-id="a524a-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-129">Un élément visuel dans un dictionnaire de ressources a l’attribut <strong>Name</strong> , qui ne peut pas être spécifié sur les enfants d’un élément <strong>ResourceDictionary</strong> .</span><span class="sxs-lookup"><span data-stu-id="a524a-129">A visual in a resource dictionary has the <strong>Name</strong> attribute, which may not be specified on any children of a <strong>ResourceDictionary</strong> element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <span data-ttu-id="a524a-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-131">Un objet portant ce nom existe déjà dans le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="a524a-131">An object with this name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <span data-ttu-id="a524a-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-133">Un objet avec ce nom de clé existe déjà dans le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="a524a-133">An object with this key name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <span data-ttu-id="a524a-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-135">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a524a-135">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <span data-ttu-id="a524a-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-137">Le rectangle de la zone de fond perdu contient une ou plusieurs valeurs qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a524a-137">The bleed box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="a524a-138">Consultez la description du paramètre pour connaître les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="a524a-138">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <span data-ttu-id="a524a-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-140">Le rectangle de la zone de contenu contient une ou plusieurs valeurs qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a524a-140">The content box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="a524a-141">Consultez la description du paramètre pour connaître les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="a524a-141">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <span data-ttu-id="a524a-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-143">La chaîne de type de contenu n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a524a-143">The content type string is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <span data-ttu-id="a524a-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-145">Une valeur <strong>float</strong> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a524a-145">A <strong>FLOAT</strong> value is not valid.</span></span> <span data-ttu-id="a524a-146">Il s’agit d’une valeur infinie ou non numérique (NAN).</span><span class="sxs-lookup"><span data-stu-id="a524a-146">It is either an infinite or not a number (NAN).</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <span data-ttu-id="a524a-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-148">L’URI de la police n’est pas valide, peut-être parce qu’il contient un ou des caractères qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="a524a-148">The font URI is not valid, possibly because it contains an empty fragment or characters that are not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <span data-ttu-id="a524a-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-150">La langue spécifiée n’est pas valide ou n’est pas correctement mise en forme.</span><span class="sxs-lookup"><span data-stu-id="a524a-150">The specified language is either not valid or not correctly formatted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <span data-ttu-id="a524a-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-152">Le nom de la clé de recherche fait référence à un objet qui n’est pas le type correct pour l’appel ; par exemple, si la méthode retourne un pinceau mais que le nom de la clé de recherche fait référence à un objet Geometry.</span><span class="sxs-lookup"><span data-stu-id="a524a-152">The lookup key name references an object that is not the correct type for the call; for example, if the method returns a brush but the lookup key name refers to a geometry object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <span data-ttu-id="a524a-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-154">Le balisage en cours de lecture contient un élément ou un attribut qui n’est pas conforme à la <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">spécification Paper XML</a>.</span><span class="sxs-lookup"><span data-stu-id="a524a-154">The markup being read contains an element or an attribute that does not conform to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a524a-155">Pour représenter des valeurs à virgule flottante, le modèle d’objet XPS utilise le type de données <strong>float</strong> au lieu de <strong>double</strong>.</span><span class="sxs-lookup"><span data-stu-id="a524a-155">To represent floating-point values, the XPS OM uses the <strong>FLOAT</strong> data type instead of <strong>DOUBLE</strong>.</span></span> <span data-ttu-id="a524a-156">Si un document XPS a un élément avec des données à virgule flottante qui ne tient pas dans une valeur <strong>float</strong> , cette erreur est retournée lorsque cette valeur est rencontrée pendant la désérialisation.</span><span class="sxs-lookup"><span data-stu-id="a524a-156">If an XPS document has an element with floating-point data that does not fit into a <strong>FLOAT</strong> value, this error will be returned when that value is encountered during deserialization.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <span data-ttu-id="a524a-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-158">La chaîne qui a été transmise n’est pas un nom valide, conformément à la spécification Paper XML.</span><span class="sxs-lookup"><span data-stu-id="a524a-158">The string that was passed is not a valid name, according to the XML Paper Specification.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <span data-ttu-id="a524a-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-160">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a524a-160">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <span data-ttu-id="a524a-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-162">Les dimensions de page contiennent une valeur de taille de page qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a524a-162">The page dimensions contain a page size value that is not valid.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <span data-ttu-id="a524a-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-164">Conformément à la <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">spécification Paper XML</a>, la chaîne de clé de recherche n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a524a-164">According to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>, the lookup key string is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <span data-ttu-id="a524a-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-166">Le type d’image miniature n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a524a-166">The thumbnail image type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <span data-ttu-id="a524a-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-168">Un balisage XML incorrect ou mis en forme de manière incorrecte a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="a524a-168">Found improper or incorrectly formatted XML markup.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <span data-ttu-id="a524a-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-170">Dans une ou plusieurs structures <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> , un élément est hors séquence.</span><span class="sxs-lookup"><span data-stu-id="a524a-170">In one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> structures, an element is out of sequence.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <span data-ttu-id="a524a-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-172">Les mappages de glyphes dépassent le nombre d’index de glyphes.</span><span class="sxs-lookup"><span data-stu-id="a524a-172">The glyph mappings exceed the number of glyph indices.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <span data-ttu-id="a524a-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-174">Erreur dans les mappages de glyphe.</span><span class="sxs-lookup"><span data-stu-id="a524a-174">Error in the glyph mappings.</span></span><br/> <span data-ttu-id="a524a-175">Si la chaîne Unicode est vide, cette erreur signifie qu’un mappage de glyphes a également été défini.</span><span class="sxs-lookup"><span data-stu-id="a524a-175">If the Unicode string is empty, this error means that a glyph mapping was also defined.</span></span> <span data-ttu-id="a524a-176">Les mappages de glyphes ne doivent pas être définis si la chaîne Unicode est vide.</span><span class="sxs-lookup"><span data-stu-id="a524a-176">Glyph mappings must not be defined if the Unicode string is empty.</span></span><br/> <span data-ttu-id="a524a-177">Si la chaîne Unicode n’est pas vide, cette erreur signifie qu’un mappage de glyphe a été défini pour les glyphes en dehors de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-177">If the Unicode string is not empty, this error means that a glyph mapping was defined for glyphs outside of the Unicode string.</span></span> <span data-ttu-id="a524a-178">Les mappages de glyphes ne peuvent pas être définis pour les glyphes qui se trouvent en dehors de la longueur de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-178">Glyph mappings cannot be defined for glyphs that fall outside the length of the Unicode string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <span data-ttu-id="a524a-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-180">Le paramètre du profil de couleurs a la <strong>valeur null</strong>, mais un profil de couleurs est attendu.</span><span class="sxs-lookup"><span data-stu-id="a524a-180">The color profile parameter is <strong>NULL</strong>, but a color profile is expected.</span></span> <span data-ttu-id="a524a-181">Un profil de couleurs est requis lorsque le type de couleur est XPS_COLOR_TYPE_CONTEXT.</span><span class="sxs-lookup"><span data-stu-id="a524a-181">A color profile is required when the color type is XPS_COLOR_TYPE_CONTEXT.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <span data-ttu-id="a524a-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-183">Une page fait référence à des ressources supprimables, mais ne spécifie pas de nom de partie DiscardControl.</span><span class="sxs-lookup"><span data-stu-id="a524a-183">A page refers to discardable resources but does not specify a DiscardControl part name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <span data-ttu-id="a524a-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter :: AddPage</strong></a> a été appelé avant <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter :: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a524a-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter::AddPage</strong></a> was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <span data-ttu-id="a524a-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-187">Le package ne contient pas de FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="a524a-187">The package does not contain a FixedDocumentSequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <span data-ttu-id="a524a-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-189">L’interface <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> requiert un URI de police, mais aucun n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="a524a-189">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface requires a font URI, but one is not specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <span data-ttu-id="a524a-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-191">L’interface <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> sans chaîne Unicode ne spécifie pas d’index de glyphes.</span><span class="sxs-lookup"><span data-stu-id="a524a-191">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface without a Unicode string does not specify any glyph indices.</span></span> <span data-ttu-id="a524a-192">Une interface <strong>IXpsOMGlyphs</strong> doit spécifier une chaîne Unicode ou un tableau d’index de glyphes.</span><span class="sxs-lookup"><span data-stu-id="a524a-192">An <strong>IXpsOMGlyphs</strong> interface must specify either a Unicode string or an array of glyph indices.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <span data-ttu-id="a524a-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-194">Une ressource d’image est introuvable pour le pinceau d’image.</span><span class="sxs-lookup"><span data-stu-id="a524a-194">An image resource could not be located for the image brush.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <span data-ttu-id="a524a-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-196">La ressource distante a un objet inattendu.</span><span class="sxs-lookup"><span data-stu-id="a524a-196">The remote resource has an unexpected object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <span data-ttu-id="a524a-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-198">La page n’a pas été nommée ; l’état de la cible du lien hypertexte ne peut être défini que si la page a un nom.</span><span class="sxs-lookup"><span data-stu-id="a524a-198">The page has not been named; the hyperlink target status can only be set if the page has a name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <span data-ttu-id="a524a-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-200">FixedDocument ne contient aucune partie FixedPage.</span><span class="sxs-lookup"><span data-stu-id="a524a-200">The FixedDocument does not contain any FixedPage parts.</span></span> <span data-ttu-id="a524a-201">Un document XPS doit contenir au moins une partie FixedPage.</span><span class="sxs-lookup"><span data-stu-id="a524a-201">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <span data-ttu-id="a524a-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-203">La référence de page n’a pas de page correspondante.</span><span class="sxs-lookup"><span data-stu-id="a524a-203">The page reference does not have a corresponding page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <span data-ttu-id="a524a-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-205">Une partie cible obligatoire n’a pas été référencée.</span><span class="sxs-lookup"><span data-stu-id="a524a-205">A required target part was not referenced.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <span data-ttu-id="a524a-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-207">Un flux n’a pas été spécifié pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="a524a-207">A stream was not specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <span data-ttu-id="a524a-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-209">La partie FixedDocument qui est référencée par FixedDocumentSequence est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a524a-209">The FixedDocument part that is referenced by the FixedDocumentSequence could not be found.</span></span> <span data-ttu-id="a524a-210">Un document XPS doit contenir au moins un FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="a524a-210">An XPS document must contain at least one FixedDocument.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <span data-ttu-id="a524a-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-212">La partie FixedPage référencée par FixedDocument est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a524a-212">The FixedPage part that is referenced by the FixedDocument could not be found.</span></span> <span data-ttu-id="a524a-213">Un document XPS doit contenir au moins une partie FixedPage.</span><span class="sxs-lookup"><span data-stu-id="a524a-213">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <span data-ttu-id="a524a-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-215">La partie cible de la relation n’est pas présente dans la relation de package.</span><span class="sxs-lookup"><span data-stu-id="a524a-215">The relationship target part is not present in the package relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <span data-ttu-id="a524a-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-217">Aucun attribut <strong>x :Key</strong> n’a été spécifié pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="a524a-217">No <strong>x:Key</strong> attribute was specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <span data-ttu-id="a524a-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-219">La ressource référencée par la page ou le contenu du dictionnaire distant n’existe pas en tant que relation de page.</span><span class="sxs-lookup"><span data-stu-id="a524a-219">The resource referred to by the page or remote dictionary content does not exist as a page relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <span data-ttu-id="a524a-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-221">La police restreinte référencée n’a pas été spécifiée dans l’appel à <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter :: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a524a-221">The referenced restricted font was not specified in the call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <span data-ttu-id="a524a-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-223">Le tableau de données de segment a moins d’entrées que le tableau de types de segments.</span><span class="sxs-lookup"><span data-stu-id="a524a-223">The segment data array has fewer entries than the segment types array.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <span data-ttu-id="a524a-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-225">Une tentative a été effectuée pour ajouter un FixedDocumentSequence à un package qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-225">An attempt was made to add a FixedDocumentSequence to a package that already has one.</span></span> <span data-ttu-id="a524a-226">Un document XPS ne doit contenir qu’une seule partie de FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="a524a-226">An XPS document must contain one and only one FixedDocumentSequence part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <span data-ttu-id="a524a-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-228">Une tentative a été effectuée pour ajouter un ticket d’impression au niveau du document à un FixedDocument qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-228">An attempt was made to add a document-level print ticket to a FixedDocument that already has one.</span></span> <span data-ttu-id="a524a-229">Un FixedDocument dans un document XPS ne peut contenir qu’un seul ticket d’impression au niveau du document.</span><span class="sxs-lookup"><span data-stu-id="a524a-229">A FixedDocument in an XPS document can contain only one document-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <span data-ttu-id="a524a-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-231">Une tentative a été effectuée pour ajouter un ticket d’impression au niveau du travail à un FixedDocumentSequence qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-231">An attempt was made to add a job-level print ticket to a FixedDocumentSequence that already has one.</span></span> <span data-ttu-id="a524a-232">Le FixedDocumentSequence dans un document XPS ne peut contenir qu’un seul ticket d’impression au niveau du travail.</span><span class="sxs-lookup"><span data-stu-id="a524a-232">The FixedDocumentSequence in an XPS document can contain only one job-level print ticket.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <span data-ttu-id="a524a-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-234">Une tentative a été effectuée pour ajouter un ticket d’impression au niveau de la page à un FixedPage qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-234">An attempt was made to add a page-level print ticket to a FixedPage that already has one.</span></span> <span data-ttu-id="a524a-235">Un FixedPage dans un document XPS ne peut contenir qu’un seul ticket d’impression au niveau de la page.</span><span class="sxs-lookup"><span data-stu-id="a524a-235">A FixedPage in an XPS document can contain only one page-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <span data-ttu-id="a524a-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-237">La collection de polices restreinte contenait une entrée de police restreinte qui a été répétée.</span><span class="sxs-lookup"><span data-stu-id="a524a-237">The restricted font collection contained a restricted font entry that was repeated.</span></span> <span data-ttu-id="a524a-238">Chaque entrée de police ne peut apparaître qu’une seule fois dans la collection.</span><span class="sxs-lookup"><span data-stu-id="a524a-238">Each font entry can occur in the collection only once.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <span data-ttu-id="a524a-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-240">Une ressource de ce nom de composant existe déjà.</span><span class="sxs-lookup"><span data-stu-id="a524a-240">A resource by that part name already exists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <span data-ttu-id="a524a-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-242">Une tentative a été effectuée pour ajouter une image miniature à un package qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-242">An attempt was made to add a thumbnail image to a package that already has one.</span></span> <span data-ttu-id="a524a-243">Un document XPS ne peut contenir qu’une seule image miniature au niveau du package.</span><span class="sxs-lookup"><span data-stu-id="a524a-243">An XPS document can contain only one package-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <span data-ttu-id="a524a-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-245">Une tentative a été effectuée pour ajouter une image miniature au niveau de la page à un FixedPage qui en a déjà un.</span><span class="sxs-lookup"><span data-stu-id="a524a-245">An attempt was made to add a page-level thumbnail image to a FixedPage that already has one.</span></span> <span data-ttu-id="a524a-246">Un FixedPage dans un document XPS ne peut contenir qu’une seule image miniature au niveau de la page.</span><span class="sxs-lookup"><span data-stu-id="a524a-246">A FixedPage in an XPS document can contain only one page-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <span data-ttu-id="a524a-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-248">Une entrée contient une valeur négative, mais elle doit contenir une valeur non négative.</span><span class="sxs-lookup"><span data-stu-id="a524a-248">An entry contains a negative value, but it must contain a non-negative value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <span data-ttu-id="a524a-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-250">Une tentative d’ajout d’une référence de dictionnaire distant à un dictionnaire distant a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="a524a-250">An attempt was made to add a remote dictionary reference to a remote dictionary.</span></span> <span data-ttu-id="a524a-251">Un dictionnaire distant ne peut pas faire référence à un autre dictionnaire distant.</span><span class="sxs-lookup"><span data-stu-id="a524a-251">A remote dictionary cannot reference another remote dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <span data-ttu-id="a524a-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-253">Un pointeur d’interface ne pointe pas vers une implémentation d’interface reconnue.</span><span class="sxs-lookup"><span data-stu-id="a524a-253">An interface pointer does not point to a recognized interface implementation.</span></span> <span data-ttu-id="a524a-254">L’implémentation personnalisée des interfaces d’API de document XPS n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a524a-254">Custom implementation of XPS Document API interfaces is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <span data-ttu-id="a524a-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-256">La collection de points de dégradé a moins de deux arrêts.</span><span class="sxs-lookup"><span data-stu-id="a524a-256">The gradient stop collection has fewer than two stops.</span></span> <span data-ttu-id="a524a-257">Une collection d’arrêts de dégradé doit avoir au moins deux points de dégradé.</span><span class="sxs-lookup"><span data-stu-id="a524a-257">A gradient stop collection must have at least two gradient stops.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <span data-ttu-id="a524a-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-259">La chaîne de texte a été spécifiée comme étant orientée latéralement et de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="a524a-259">The text string was specified as being oriented sideways and right-to-left.</span></span> <span data-ttu-id="a524a-260">Si le texte est orienté latéralement, il ne peut pas avoir un niveau bidi qui est une valeur impaire (de droite à gauche).</span><span class="sxs-lookup"><span data-stu-id="a524a-260">If the text is oriented sideways, it cannot have a bidi level that is an odd value (right-to-left).</span></span> <span data-ttu-id="a524a-261">De même, si le niveau bidi est une valeur impaire, le texte ne peut pas être orienté latéralement.</span><span class="sxs-lookup"><span data-stu-id="a524a-261">Likewise, if the bidi level is an odd value, the text cannot be oriented sideways.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <span data-ttu-id="a524a-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-263">Les mappages de glyphes ne correspondent pas au contenu de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-263">The glyph mappings do not match the Unicode string contents.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <span data-ttu-id="a524a-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-265">Le writer de package n’a pas été fermé avant sa sortie.</span><span class="sxs-lookup"><span data-stu-id="a524a-265">The package writer was not closed before it was released.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <span data-ttu-id="a524a-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-267">Une relation fait référence à un composant qui se trouve en dehors du document XPS.</span><span class="sxs-lookup"><span data-stu-id="a524a-267">A relationship refers to a part that is outside of the XPS document.</span></span> <span data-ttu-id="a524a-268">Tout le contenu à restituer dans un document XPS doit être contenu dans le document XPS.</span><span class="sxs-lookup"><span data-stu-id="a524a-268">All content to be rendered in an XPS document must be contained in the XPS document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <span data-ttu-id="a524a-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-270">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a524a-270">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <span data-ttu-id="a524a-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-272"><em>Réservé</em>.</span><span class="sxs-lookup"><span data-stu-id="a524a-272"><em>Reserved</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <span data-ttu-id="a524a-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-274">Un dépassement de capacité <strong>size_t</strong> s’est produit lors d’une tentative de copie d’une chaîne dans une nouvelle mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a524a-274">A <strong>size_t</strong> overflow occurred during an attempt to copy a string into a new buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <span data-ttu-id="a524a-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-276">Il existait plus d’index de glyphes que de points de code Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-276">There were more glyph indices than Unicode code points.</span></span> <span data-ttu-id="a524a-277">S’il n’existe aucun mappage de glyphe, le nombre d’index de glyphes doit être inférieur ou égal au nombre de points de code Unicode.</span><span class="sxs-lookup"><span data-stu-id="a524a-277">If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of Unicode code points.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <span data-ttu-id="a524a-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-279">Une erreur grave s’est produite et le contenu du modèle d’objet XPS peut être irrécupérable.</span><span class="sxs-lookup"><span data-stu-id="a524a-279">A severe error occurred and the contents of the XPS OM might be unrecoverable.</span></span> <span data-ttu-id="a524a-280">Certains composants du modèle d’objet XPS peuvent toujours être utilisables, mais ils devront être vérifiés avant d’être utilisés.</span><span class="sxs-lookup"><span data-stu-id="a524a-280">Some components of the XPS OM might still be usable, but they will need to be verified before being used further.</span></span> <span data-ttu-id="a524a-281">Étant donné que l’état du modèle d’objet XPS ne peut pas être prédit après le retour de cette erreur, tous les composants du modèle d’objet XPS doivent être libérés et ignorés.</span><span class="sxs-lookup"><span data-stu-id="a524a-281">Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <span data-ttu-id="a524a-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-283">Un profil de couleurs était présent lorsqu’il n’était pas attendu.</span><span class="sxs-lookup"><span data-stu-id="a524a-283">A color profile was present when one was not expected.</span></span> <span data-ttu-id="a524a-284">Un profil de couleurs est uniquement autorisé lorsque le type de couleur est <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a524a-284">A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <span data-ttu-id="a524a-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-286">La cible d’une relation n’est pas le type attendu par le contexte de la relation.</span><span class="sxs-lookup"><span data-stu-id="a524a-286">The target of a relationship is not the type expected by the context of the relationship.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <span data-ttu-id="a524a-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-288">Le type de relation n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="a524a-288">The relationship type was not recognized.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <span data-ttu-id="a524a-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-290">La collection de polices restreinte contient une police non restreinte.</span><span class="sxs-lookup"><span data-stu-id="a524a-290">The restricted font collection contains an unrestricted font.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <span data-ttu-id="a524a-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-292">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a524a-292">Reserved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <span data-ttu-id="a524a-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span><span class="sxs-lookup"><span data-stu-id="a524a-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span></span></dl></td>
<td><span data-ttu-id="a524a-294">Une géométrie de chemin d’accès qui ne se trouve pas dans un dictionnaire de ressources a un attribut <strong>x :Key</strong> spécifié.</span><span class="sxs-lookup"><span data-stu-id="a524a-294">A path geometry that is not in a resource dictionary has an <strong>x:Key</strong> attribute specified.</span></span> <span data-ttu-id="a524a-295">Les géométries de tracés qui ne sont pas dans un dictionnaire de ressources ne peuvent pas avoir d’attribut <strong>x :Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="a524a-295">Path geometries that are not in a resource dictionary cannot have an <strong>x:Key</strong> attribute.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a524a-296">Notes</span><span class="sxs-lookup"><span data-stu-id="a524a-296">Remarks</span></span>

<span data-ttu-id="a524a-297">Certaines méthodes de l’API de document XPS effectuent des appels à l’API de [Packaging](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="a524a-297">Some XPS document API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="a524a-298">Pour plus d’informations sur les valeurs de retour de l’API de Packaging, consultez [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="a524a-298">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="a524a-299">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a524a-299">Requirements</span></span>



| <span data-ttu-id="a524a-300">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a524a-300">Requirement</span></span> | <span data-ttu-id="a524a-301">Valeur</span><span class="sxs-lookup"><span data-stu-id="a524a-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a524a-302">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a524a-302">Minimum supported client</span></span><br/> | <span data-ttu-id="a524a-303">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a524a-303">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a524a-304">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a524a-304">Minimum supported server</span></span><br/> | <span data-ttu-id="a524a-305">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de plateforme pour les applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a524a-305">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a524a-306">En-tête</span><span class="sxs-lookup"><span data-stu-id="a524a-306">Header</span></span><br/>                   | <dl> <span data-ttu-id="a524a-307"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="a524a-307"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                       |
| <span data-ttu-id="a524a-308">MIDL</span><span class="sxs-lookup"><span data-stu-id="a524a-308">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a524a-309"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a524a-309"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                     |



## <a name="see-also"></a><span data-ttu-id="a524a-310">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a524a-310">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a524a-311">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="a524a-311">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> </dl>

 

