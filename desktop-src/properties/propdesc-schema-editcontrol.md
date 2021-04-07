---
description: Spécifie le contrôle à utiliser lors de la modification de la propriété.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: editControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952080"
---
# <a name="editcontrol"></a><span data-ttu-id="4874d-103">editControl</span><span class="sxs-lookup"><span data-stu-id="4874d-103">editControl</span></span>

<span data-ttu-id="4874d-104">Spécifie le contrôle à utiliser lors de la modification de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4874d-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="4874d-105">Il ne doit y avoir qu’un seul élément [editControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4874d-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="4874d-106">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4874d-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="4874d-107">Si aucun élément [editControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="4874d-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="4874d-108">Si <typeInfo isInnate="true"> , cet élément est ignoré, car une propriété innée ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="4874d-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="4874d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4874d-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="4874d-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4874d-110">Element Information</span></span>



| <span data-ttu-id="4874d-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="4874d-111">Parent Element</span></span>                                   | <span data-ttu-id="4874d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4874d-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="4874d-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="4874d-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="4874d-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="4874d-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="4874d-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="4874d-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4874d-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="4874d-116">Attribute</span></span></th>
<th><span data-ttu-id="4874d-117">Description</span><span class="sxs-lookup"><span data-stu-id="4874d-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4874d-118">contrôle</span><span class="sxs-lookup"><span data-stu-id="4874d-118">control</span></span></td>
<td><span data-ttu-id="4874d-119">Public.</span><span class="sxs-lookup"><span data-stu-id="4874d-119">Public.</span></span> <span data-ttu-id="4874d-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4874d-120">Optional.</span></span> <span data-ttu-id="4874d-121">La valeur par défaut est &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="4874d-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="4874d-122">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="4874d-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4874d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4874d-123">Value</span></span></th>
<th><span data-ttu-id="4874d-124">Signification</span><span class="sxs-lookup"><span data-stu-id="4874d-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4874d-125">Default</span><span class="sxs-lookup"><span data-stu-id="4874d-125">Default</span></span></td>
<td><span data-ttu-id="4874d-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="4874d-126">Default.</span></span> <span data-ttu-id="4874d-127">Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut.</span><span class="sxs-lookup"><span data-stu-id="4874d-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="4874d-128">Les types par défaut sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="4874d-128">The default types are listed below.</span></span> <span data-ttu-id="4874d-129">Tout autre type entraîne l’utilisation du &quot; contrôle de texte &quot; .</span><span class="sxs-lookup"><span data-stu-id="4874d-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4874d-130">Type</span><span class="sxs-lookup"><span data-stu-id="4874d-130">Type</span></span></th>
<th><span data-ttu-id="4874d-131">Contrôler</span><span class="sxs-lookup"><span data-stu-id="4874d-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4874d-132">String</span><span class="sxs-lookup"><span data-stu-id="4874d-132">String</span></span></td>
<td><span data-ttu-id="4874d-133">Texte</span><span class="sxs-lookup"><span data-stu-id="4874d-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4874d-134">Chaîne (valeurs multiples)</span><span class="sxs-lookup"><span data-stu-id="4874d-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="4874d-135">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="4874d-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4874d-136">DateTime</span><span class="sxs-lookup"><span data-stu-id="4874d-136">DateTime</span></span></td>
<td><span data-ttu-id="4874d-137">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4874d-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4874d-138">Calendrier</span><span class="sxs-lookup"><span data-stu-id="4874d-138">Calendar</span></span></td>
<td><span data-ttu-id="4874d-139">Utilise le contrôle calendrier.</span><span class="sxs-lookup"><span data-stu-id="4874d-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4874d-140">CheckboxDropList</span><span class="sxs-lookup"><span data-stu-id="4874d-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="4874d-141">Utilise le contrôle de liste avec des cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="4874d-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4874d-142">Roulant</span><span class="sxs-lookup"><span data-stu-id="4874d-142">DropList</span></span></td>
<td><span data-ttu-id="4874d-143">Utilise le contrôle de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="4874d-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4874d-144">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="4874d-144">MultiLineText</span></span></td>
<td><span data-ttu-id="4874d-145">Utilise le contrôle d’édition de texte sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="4874d-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4874d-146">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="4874d-146">MultiValueText</span></span></td>
<td><span data-ttu-id="4874d-147">Utilise le contrôle d’édition de texte à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="4874d-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4874d-148">Rating</span><span class="sxs-lookup"><span data-stu-id="4874d-148">Rating</span></span></td>
<td><span data-ttu-id="4874d-149">Utilise le contrôle d’évaluation 5 étoiles.</span><span class="sxs-lookup"><span data-stu-id="4874d-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4874d-150">Texte</span><span class="sxs-lookup"><span data-stu-id="4874d-150">Text</span></span></td>
<td><span data-ttu-id="4874d-151">Utilise le contrôle d’édition de texte.</span><span class="sxs-lookup"><span data-stu-id="4874d-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4874d-152">IconList</span><span class="sxs-lookup"><span data-stu-id="4874d-152">IconList</span></span></td>
<td><span data-ttu-id="4874d-153"><strong>Windows 7 et versions ultérieures.</strong></span><span class="sxs-lookup"><span data-stu-id="4874d-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
