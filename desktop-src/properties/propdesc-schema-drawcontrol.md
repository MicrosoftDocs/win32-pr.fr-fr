---
description: Spécifie le contrôle à utiliser lors de l’affichage de la propriété.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: drawControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034284"
---
# <a name="drawcontrol"></a><span data-ttu-id="a729f-103">drawControl</span><span class="sxs-lookup"><span data-stu-id="a729f-103">drawControl</span></span>

<span data-ttu-id="a729f-104">Spécifie le contrôle à utiliser lors de l’affichage de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a729f-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="a729f-105">Il ne doit y avoir qu’un seul élément [drawControl]() pour chaque élément [displayInfo](./propdesc-schema-displayinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a729f-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="a729f-106">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a729f-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="a729f-107">Si aucun élément [drawControl]() n’est fourni, les paramètres d’attribut par défaut sont appliqués à la description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a729f-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="a729f-108">Cette forme du contrôle n’autorise pas la modification de propriété.</span><span class="sxs-lookup"><span data-stu-id="a729f-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a729f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a729f-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="a729f-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a729f-110">Element Information</span></span>



| <span data-ttu-id="a729f-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="a729f-111">Parent Element</span></span>                                   | <span data-ttu-id="a729f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a729f-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="a729f-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a729f-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="a729f-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="a729f-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="a729f-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="a729f-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a729f-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="a729f-116">Attribute</span></span></th>
<th><span data-ttu-id="a729f-117">Description</span><span class="sxs-lookup"><span data-stu-id="a729f-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a729f-118">contrôle</span><span class="sxs-lookup"><span data-stu-id="a729f-118">control</span></span></td>
<td><span data-ttu-id="a729f-119">Public.</span><span class="sxs-lookup"><span data-stu-id="a729f-119">Public.</span></span> <span data-ttu-id="a729f-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="a729f-120">Optional.</span></span> <span data-ttu-id="a729f-121">La valeur par défaut est &quot; default &quot; .</span><span class="sxs-lookup"><span data-stu-id="a729f-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="a729f-122">Les valeurs valides sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="a729f-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a729f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a729f-123">Value</span></span></th>
<th><span data-ttu-id="a729f-124">Signification</span><span class="sxs-lookup"><span data-stu-id="a729f-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a729f-125">Default</span><span class="sxs-lookup"><span data-stu-id="a729f-125">Default</span></span></td>
<td><span data-ttu-id="a729f-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a729f-126">Default.</span></span> <span data-ttu-id="a729f-127">Utilise le contrôle par défaut basé sur l' <typeInfo type=&quot;&quot;> attribut.</span><span class="sxs-lookup"><span data-stu-id="a729f-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="a729f-128">Le type par défaut est &quot; String &quot; (valeur multiple) et le contrôle par défaut est &quot; MultiValueText &quot; .</span><span class="sxs-lookup"><span data-stu-id="a729f-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="a729f-129">Tout autre type entraîne l’utilisation du &quot; &quot; contrôle StaticText.</span><span class="sxs-lookup"><span data-stu-id="a729f-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a729f-130">MultiLineText</span><span class="sxs-lookup"><span data-stu-id="a729f-130">MultiLineText</span></span></td>
<td><span data-ttu-id="a729f-131">Utilise le contrôle de texte sur plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="a729f-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a729f-132">MultiValueText</span><span class="sxs-lookup"><span data-stu-id="a729f-132">MultiValueText</span></span></td>
<td><span data-ttu-id="a729f-133">Utilise le contrôle de texte à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="a729f-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a729f-134">PercentBar</span><span class="sxs-lookup"><span data-stu-id="a729f-134">PercentBar</span></span></td>
<td><span data-ttu-id="a729f-135">Utilise le contrôle de barre de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="a729f-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a729f-136">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="a729f-136">ProgressBar</span></span></td>
<td><span data-ttu-id="a729f-137">Utilise le contrôle de barre de progression.</span><span class="sxs-lookup"><span data-stu-id="a729f-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a729f-138">Rating</span><span class="sxs-lookup"><span data-stu-id="a729f-138">Rating</span></span></td>
<td><span data-ttu-id="a729f-139">Utilise le contrôle d’évaluation 5 étoiles.</span><span class="sxs-lookup"><span data-stu-id="a729f-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a729f-140">StaticText</span><span class="sxs-lookup"><span data-stu-id="a729f-140">StaticText</span></span></td>
<td><span data-ttu-id="a729f-141">Utilise <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription :: FormatForDisplay</strong></a> pour afficher la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="a729f-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a729f-142">IconList</span><span class="sxs-lookup"><span data-stu-id="a729f-142">IconList</span></span></td>
<td><span data-ttu-id="a729f-143"><strong>Windows 7 et versions ultérieures.</strong></span><span class="sxs-lookup"><span data-stu-id="a729f-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="a729f-144">Énumération d’icônes.</span><span class="sxs-lookup"><span data-stu-id="a729f-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a729f-145">BooleanCheckMark</span><span class="sxs-lookup"><span data-stu-id="a729f-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="a729f-146"><strong>Windows 7 et versions ultérieures.</strong></span><span class="sxs-lookup"><span data-stu-id="a729f-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
