---
description: Non pris en charge dans Windows 7 et versions ultérieures. Spécifie le contrôle à utiliser dans le générateur de requêtes.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: queryControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516995"
---
# <a name="querycontrol"></a><span data-ttu-id="928e4-104">queryControl</span><span class="sxs-lookup"><span data-stu-id="928e4-104">queryControl</span></span>

<span data-ttu-id="928e4-105">Non pris en charge dans Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="928e4-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="928e4-106">Spécifie le contrôle à utiliser dans le générateur de requêtes.</span><span class="sxs-lookup"><span data-stu-id="928e4-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="928e4-107">Il ne doit y avoir qu’un seul élément [queryControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="928e4-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="928e4-108">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="928e4-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="928e4-109">Si aucun élément [queryControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="928e4-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="928e4-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="928e4-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="928e4-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="928e4-111">Element Information</span></span>



| <span data-ttu-id="928e4-112">Élément parent</span><span class="sxs-lookup"><span data-stu-id="928e4-112">Parent Element</span></span>                                   | <span data-ttu-id="928e4-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="928e4-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="928e4-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="928e4-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="928e4-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="928e4-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="928e4-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="928e4-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="928e4-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="928e4-117">Attribute</span></span></th>
<th><span data-ttu-id="928e4-118">Description</span><span class="sxs-lookup"><span data-stu-id="928e4-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="928e4-119">contrôle</span><span class="sxs-lookup"><span data-stu-id="928e4-119">control</span></span></td>
<td><span data-ttu-id="928e4-120">Public.</span><span class="sxs-lookup"><span data-stu-id="928e4-120">Public.</span></span> <span data-ttu-id="928e4-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="928e4-121">Optional.</span></span> <span data-ttu-id="928e4-122">La valeur par défaut est &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="928e4-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="928e4-123">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="928e4-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="928e4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="928e4-124">Value</span></span></th>
<th><span data-ttu-id="928e4-125">Signification</span><span class="sxs-lookup"><span data-stu-id="928e4-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="928e4-126">Default</span><span class="sxs-lookup"><span data-stu-id="928e4-126">Default</span></span></td>
<td><span data-ttu-id="928e4-127">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="928e4-127">Default.</span></span> <span data-ttu-id="928e4-128">Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut.</span><span class="sxs-lookup"><span data-stu-id="928e4-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="928e4-129">Les types par défaut sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="928e4-129">The default types are listed below.</span></span> <span data-ttu-id="928e4-130">Tout autre type entraîne l’utilisation du &quot; contrôle de texte &quot; .</span><span class="sxs-lookup"><span data-stu-id="928e4-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="928e4-131">ConditionType</span><span class="sxs-lookup"><span data-stu-id="928e4-131">ConditionType</span></span></th>
<th><span data-ttu-id="928e4-132">Contrôler</span><span class="sxs-lookup"><span data-stu-id="928e4-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="928e4-133">String</span><span class="sxs-lookup"><span data-stu-id="928e4-133">String</span></span></td>
<td><span data-ttu-id="928e4-134">Texte</span><span class="sxs-lookup"><span data-stu-id="928e4-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-135">Chaîne (valeurs multiples)</span><span class="sxs-lookup"><span data-stu-id="928e4-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="928e4-136">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="928e4-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-137">Nombre ou taille</span><span class="sxs-lookup"><span data-stu-id="928e4-137">Number or Size</span></span></td>
<td><span data-ttu-id="928e4-138">NumericText</span><span class="sxs-lookup"><span data-stu-id="928e4-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-139">Nombre ou taille (enum)</span><span class="sxs-lookup"><span data-stu-id="928e4-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="928e4-140">List</span><span class="sxs-lookup"><span data-stu-id="928e4-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-141">DateTime</span><span class="sxs-lookup"><span data-stu-id="928e4-141">DateTime</span></span></td>
<td><span data-ttu-id="928e4-142">Calendrier</span><span class="sxs-lookup"><span data-stu-id="928e4-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="928e4-143">Boolean</span></span></td>
<td><span data-ttu-id="928e4-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="928e4-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="928e4-145">Boolean</span></span></td>
<td><span data-ttu-id="928e4-146">Utilise le contrôle booléen.</span><span class="sxs-lookup"><span data-stu-id="928e4-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-147">Calendrier</span><span class="sxs-lookup"><span data-stu-id="928e4-147">Calendar</span></span></td>
<td><span data-ttu-id="928e4-148">Utilise le contrôle de calendrier déroulant.</span><span class="sxs-lookup"><span data-stu-id="928e4-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-149">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="928e4-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="928e4-150">Utilise le contrôle de liste avec des cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="928e4-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-151">Roulant</span><span class="sxs-lookup"><span data-stu-id="928e4-151">DropList</span></span></td>
<td><span data-ttu-id="928e4-152">Utilise le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="928e4-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-153">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="928e4-153">MultiValueText</span></span></td>
<td><span data-ttu-id="928e4-154">Utilise le contrôle d’édition de texte à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="928e4-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-155">NumericText</span><span class="sxs-lookup"><span data-stu-id="928e4-155">NumericText</span></span></td>
<td><span data-ttu-id="928e4-156">Utilise le contrôle d’édition de texte numérique.</span><span class="sxs-lookup"><span data-stu-id="928e4-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="928e4-157">Rating</span><span class="sxs-lookup"><span data-stu-id="928e4-157">Rating</span></span></td>
<td><span data-ttu-id="928e4-158">Utilise le contrôle d’évaluation 5 étoiles.</span><span class="sxs-lookup"><span data-stu-id="928e4-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="928e4-159">Texte</span><span class="sxs-lookup"><span data-stu-id="928e4-159">Text</span></span></td>
<td><span data-ttu-id="928e4-160">Utilise le contrôle d’édition de texte.</span><span class="sxs-lookup"><span data-stu-id="928e4-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
