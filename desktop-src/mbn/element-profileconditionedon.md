---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112911"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span data-ttu-id="e65ca-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span><span class="sxs-lookup"><span data-stu-id="e65ca-103"><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn</span></span>

<span data-ttu-id="e65ca-104">Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</span><span class="sxs-lookup"><span data-stu-id="e65ca-104">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span>

<span data-ttu-id="e65ca-105">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="e65ca-105">This element is new for v4.</span></span> <span data-ttu-id="e65ca-106">Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable.</span><span class="sxs-lookup"><span data-stu-id="e65ca-106">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="e65ca-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e65ca-107">This element is optional.</span></span> <span data-ttu-id="e65ca-108">Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</span><span class="sxs-lookup"><span data-stu-id="e65ca-108">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="e65ca-109">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="e65ca-109">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a><span data-ttu-id="e65ca-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e65ca-110">Syntax</span></span>

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a><span data-ttu-id="e65ca-111">Clé</span><span class="sxs-lookup"><span data-stu-id="e65ca-111">Key</span></span>

<span data-ttu-id="e65ca-112">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="e65ca-112">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="e65ca-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e65ca-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="e65ca-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="e65ca-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="e65ca-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="e65ca-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="e65ca-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e65ca-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e65ca-117">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="e65ca-117">Child Element</span></span></th>
<th><span data-ttu-id="e65ca-118">Description</span><span class="sxs-lookup"><span data-stu-id="e65ca-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e65ca-119"><a href="element-cellularclass.md">CellularClass</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-119"><a href="element-cellularclass.md">CellularClass</a></span></span></td>
<td><p><span data-ttu-id="e65ca-120">Spécifie que ce profil est actif uniquement lorsque la classe cellulaire actuelle est celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e65ca-120">Specifies that this profile is active only when the current cellular class is the one specified.</span></span> <span data-ttu-id="e65ca-121">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e65ca-121">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ca-122"><a href="element-imsi.md">IMSI</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-122"><a href="element-imsi.md">IMSI</a></span></span></td>
<td><p><span data-ttu-id="e65ca-123">Spécifie que ce profil est actif uniquement lorsque la IMSI actuelle utilisée dans le ICCID est celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e65ca-123">Specifies that this profile is active only when the current IMSI being used in the ICCID is the one specified.</span></span> <span data-ttu-id="e65ca-124">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e65ca-124">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ca-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-125"><a href="element-iwlanapplicability.md">IwlanApplicability</a></span></span></td>
<td><p><span data-ttu-id="e65ca-126">Spécifie que ce profil est actif uniquement lorsqu’il est connecté à un réseau IWLAN.</span><span class="sxs-lookup"><span data-stu-id="e65ca-126">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="e65ca-127">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e65ca-127">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="e65ca-128">La valeur de cet élément doit être une valeur <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> valide.</span><span class="sxs-lookup"><span data-stu-id="e65ca-128">The value of this element must be a valid <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ca-129"><a href="element-ratapplicability.md">RATApplicability</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-129"><a href="element-ratapplicability.md">RATApplicability</a></span></span></td>
<td><p><span data-ttu-id="e65ca-130">Spécifie que ce profil est actif uniquement lorsque le type de RAT est celui spécifié.</span><span class="sxs-lookup"><span data-stu-id="e65ca-130">Specifies that this profile is active only when the RAT type is the one specified.</span></span> <span data-ttu-id="e65ca-131">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e65ca-131">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ca-132"><a href="element-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-132"><a href="element-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="e65ca-133">Spécifie que ce profil est actif uniquement lorsque la condition d’itinérance actuelle est celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e65ca-133">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="e65ca-134">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e65ca-134">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="e65ca-135">La valeur de cet élément doit être une valeur <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valide.</span><span class="sxs-lookup"><span data-stu-id="e65ca-135">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="e65ca-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e65ca-136"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e65ca-137">Élément parent</span><span class="sxs-lookup"><span data-stu-id="e65ca-137">Parent Element</span></span></th>
<th><span data-ttu-id="e65ca-138">Description</span><span class="sxs-lookup"><span data-stu-id="e65ca-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e65ca-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="e65ca-139"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="e65ca-140">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="e65ca-140">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="e65ca-141">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="e65ca-141">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="e65ca-142">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="e65ca-142">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="e65ca-143">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="e65ca-143">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="e65ca-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e65ca-144">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e65ca-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e65ca-145">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



