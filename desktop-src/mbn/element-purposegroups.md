---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 370cf6b0dc13848ca21a2a06e0b9806d753878c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533595"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span data-ttu-id="35efc-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span><span class="sxs-lookup"><span data-stu-id="35efc-103"><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups</span></span>

<span data-ttu-id="35efc-104">Liste facultative de groupes de profils, où chaque groupe comprend des profils utilisés dans un but commun.</span><span class="sxs-lookup"><span data-stu-id="35efc-104">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span>

<span data-ttu-id="35efc-105">Cet élément est une nouveauté pour v4 du schéma.</span><span class="sxs-lookup"><span data-stu-id="35efc-105">This element is new for v4 of the schema.</span></span>

<span data-ttu-id="35efc-106">Un profil peut être listé dans plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="35efc-106">One profile can be listed in multiple groups.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="35efc-107">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="35efc-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a><span data-ttu-id="35efc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35efc-108">Syntax</span></span>

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a><span data-ttu-id="35efc-109">Clé</span><span class="sxs-lookup"><span data-stu-id="35efc-109">Key</span></span>

<span data-ttu-id="35efc-110">`{}`   plage spécifique d’occurrences</span><span class="sxs-lookup"><span data-stu-id="35efc-110">`{}`   specific range of occurrences</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="35efc-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="35efc-111"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="35efc-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="35efc-112"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="35efc-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="35efc-113">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="35efc-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="35efc-114"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35efc-115">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="35efc-115">Child Element</span></span></th>
<th><span data-ttu-id="35efc-116">Description</span><span class="sxs-lookup"><span data-stu-id="35efc-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35efc-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span><span class="sxs-lookup"><span data-stu-id="35efc-117"><a href="element-purposegroupguid.md">PurposeGroupGuid</a></span></span></td>
<td><p><span data-ttu-id="35efc-118">Représente un profil dans un PurposeGroup de profils.</span><span class="sxs-lookup"><span data-stu-id="35efc-118">Represents one profile in a PurposeGroup of profiles.</span></span></p>
<p><span data-ttu-id="35efc-119">Les profils sont spécifiés par leur valeur <a href="simpletype-guidtype.md"><strong>guidType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="35efc-119">Profiles are specified by their <a href="simpletype-guidtype.md"><strong>guidType</strong></a> value.</span></span></p>
<p><span data-ttu-id="35efc-120">Quatre valeurs GUID sont définies, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="35efc-120">Four GUID values are defined, as listed in the following table.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="35efc-121">Groupe d’objectifs</span><span class="sxs-lookup"><span data-stu-id="35efc-121">Purpose group</span></span></th>
<th><span data-ttu-id="35efc-122">GUID</span><span class="sxs-lookup"><span data-stu-id="35efc-122">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35efc-123">Internet</span><span class="sxs-lookup"><span data-stu-id="35efc-123">Internet</span></span></td>
<td><span data-ttu-id="35efc-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span><span class="sxs-lookup"><span data-stu-id="35efc-124">3E5545D2-1137-4DC8-A198-33F1C657515F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35efc-125">mms</span><span class="sxs-lookup"><span data-stu-id="35efc-125">MMS</span></span></td>
<td><span data-ttu-id="35efc-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span><span class="sxs-lookup"><span data-stu-id="35efc-126">53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35efc-127">IMS</span><span class="sxs-lookup"><span data-stu-id="35efc-127">IMS</span></span></td>
<td><span data-ttu-id="35efc-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span><span class="sxs-lookup"><span data-stu-id="35efc-128">474D66ED-0E4B-476B-A455-19BB1239ED13</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35efc-129">SUPL</span><span class="sxs-lookup"><span data-stu-id="35efc-129">SUPL</span></span></td>
<td><span data-ttu-id="35efc-130">6D42669F-52A9-408E-9493-1071DCC437BD</span><span class="sxs-lookup"><span data-stu-id="35efc-130">6D42669F-52A9-408E-9493-1071DCC437BD</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="35efc-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="35efc-131"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35efc-132">Élément parent</span><span class="sxs-lookup"><span data-stu-id="35efc-132">Parent Element</span></span></th>
<th><span data-ttu-id="35efc-133">Description</span><span class="sxs-lookup"><span data-stu-id="35efc-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35efc-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="35efc-134"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="35efc-135">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="35efc-135">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="35efc-136">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="35efc-136">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="35efc-137">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="35efc-137">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="35efc-138">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="35efc-138">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="35efc-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35efc-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="35efc-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="35efc-140">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



