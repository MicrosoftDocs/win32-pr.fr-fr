---
description: Spécifie la façon dont les étiquettes de la propriété sont affichées.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527819"
---
# <a name="labelinfo"></a><span data-ttu-id="f9b78-103">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f9b78-103">labelInfo</span></span>

<span data-ttu-id="f9b78-104">Spécifie la façon dont les étiquettes de la propriété sont affichées.</span><span class="sxs-lookup"><span data-stu-id="f9b78-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="f9b78-105">Il ne doit y avoir qu’un seul élément [labelInfo]() pour chaque élément [PropertyDescription](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="f9b78-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="f9b78-106">S’il y a plusieurs éléments, le dernier est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f9b78-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="f9b78-107">Si aucun élément [labelInfo]() n’est fourni, l’étiquette de la propriété n’est pas affichée ; Toutefois, il s’agit généralement d’un défaut.</span><span class="sxs-lookup"><span data-stu-id="f9b78-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b78-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9b78-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="f9b78-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f9b78-109">Element Information</span></span>



| <span data-ttu-id="f9b78-110">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f9b78-110">Parent Element</span></span>                                                   | <span data-ttu-id="f9b78-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f9b78-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f9b78-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f9b78-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="f9b78-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="f9b78-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="f9b78-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="f9b78-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9b78-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="f9b78-115">Attribute</span></span></th>
<th><span data-ttu-id="f9b78-116">Description</span><span class="sxs-lookup"><span data-stu-id="f9b78-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9b78-117">label</span><span class="sxs-lookup"><span data-stu-id="f9b78-117">label</span></span></td>
<td><span data-ttu-id="f9b78-118">Public.</span><span class="sxs-lookup"><span data-stu-id="f9b78-118">Public.</span></span> <span data-ttu-id="f9b78-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f9b78-119">Optional.</span></span> <span data-ttu-id="f9b78-120">Étiquette telle qu’elle s’affiche dans l’interface utilisateur (par exemple, l’étiquette de la colonne Détails ou le volet de visualisation).</span><span class="sxs-lookup"><span data-stu-id="f9b78-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="f9b78-121">La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte.</span><span class="sxs-lookup"><span data-stu-id="f9b78-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="f9b78-122">Utilisez la chaîne d’affichage indirecte, car elle peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="f9b78-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="f9b78-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription :: GetDisplayName</strong></a> retourne le nom complet résolu.</span><span class="sxs-lookup"><span data-stu-id="f9b78-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b78-124">sortDescription</span><span class="sxs-lookup"><span data-stu-id="f9b78-124">sortDescription</span></span></td>
<td><span data-ttu-id="f9b78-125">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f9b78-125">Optional.</span></span> <span data-ttu-id="f9b78-126">Spécifie les chaînes proposées en tant qu’options de tri.</span><span class="sxs-lookup"><span data-stu-id="f9b78-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="f9b78-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription :: GetSortDescription</strong></a> retourne cette description de tri.</span><span class="sxs-lookup"><span data-stu-id="f9b78-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="f9b78-128">Les valeurs suivantes fournissent les chaînes d’interface utilisateur correspondantes.</span><span class="sxs-lookup"><span data-stu-id="f9b78-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="f9b78-129">Général : tri en cours de tri en cours &quot; &quot;  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="f9b78-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="f9b78-130">AToZ : &quot; A sur &quot;  /  &quot; Z supérieur en haut&quot;</span><span class="sxs-lookup"><span data-stu-id="f9b78-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="f9b78-131">LowestHighest : &quot; du plus petit au &quot;  /  &quot; plus haut en haut&quot;</span><span class="sxs-lookup"><span data-stu-id="f9b78-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="f9b78-132">OldestNewest : &quot; du plus ancien au plus &quot;  /  &quot; récent en haut&quot;</span><span class="sxs-lookup"><span data-stu-id="f9b78-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="f9b78-133">SmallestLargest : &quot; le plus petit au &quot;  /  &quot; plus grand en haut&quot;</span><span class="sxs-lookup"><span data-stu-id="f9b78-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9b78-134">invitationText</span><span class="sxs-lookup"><span data-stu-id="f9b78-134">invitationText</span></span></td>
<td><span data-ttu-id="f9b78-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f9b78-135">Optional.</span></span> <span data-ttu-id="f9b78-136">Texte de la chaîne d’aide affiché en tant qu’instruction à l’utilisateur pour le contrôle ou l’info-bulle (par exemple, entrez le nom de l' &quot; auteur &quot; ).</span><span class="sxs-lookup"><span data-stu-id="f9b78-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="f9b78-137">La syntaxe autorise une chaîne d’affichage directe ou une référence à une chaîne d’affichage indirecte.</span><span class="sxs-lookup"><span data-stu-id="f9b78-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="f9b78-138">Utilisez la chaîne d’affichage indirecte, car elle peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="f9b78-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="f9b78-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription :: GetEditInvitation</strong></a> retourne le texte d’invitation résolu.</span><span class="sxs-lookup"><span data-stu-id="f9b78-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9b78-140">hideLabel</span><span class="sxs-lookup"><span data-stu-id="f9b78-140">hideLabel</span></span></td>
<td><span data-ttu-id="f9b78-141">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f9b78-141">Optional.</span></span> <span data-ttu-id="f9b78-142">La valeur par défaut est &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="f9b78-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="f9b78-143">Indique si l’étiquette est masquée.</span><span class="sxs-lookup"><span data-stu-id="f9b78-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
