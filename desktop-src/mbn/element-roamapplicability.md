---
description: MBNProfileExt \/ RoamApplicability (v4)
MS-HAID: WWAN\_profile\_v4.element\_RoamApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RoamApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29438df96a3a12bb791870b1cc0d59e84f77d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516654"
---
# <a name="span-idwwan_profile_v4element_roamapplicabilityspanmbnprofileextroamapplicability-v4"></a><span data-ttu-id="91cb2-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt \/ RoamApplicability (v4)</span><span class="sxs-lookup"><span data-stu-id="91cb2-103"><span id="WWAN_profile_v4.element_RoamApplicability"></span>MBNProfileExt\/RoamApplicability (v4)</span></span>

<span data-ttu-id="91cb2-104">Spécifie que ce profil est actif uniquement lorsque la condition d’itinérance actuelle est celle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="91cb2-104">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="91cb2-105">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="91cb2-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="91cb2-106">La valeur de cet élément doit être une valeur [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) valide.</span><span class="sxs-lookup"><span data-stu-id="91cb2-106">The value of this element must be a valid [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="91cb2-107">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="91cb2-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<RoamApplicability\>**

## <a name="syntax"></a><span data-ttu-id="91cb2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91cb2-108">Syntax</span></span>

``` syntax
<RoamApplicability>

  "NonPartnerOnly" | "PartnerOnly" | "HomeOnly" | "HomeAndPartner" | "PartnerAndNonpartner" | "AllRoaming"

</RoamApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="91cb2-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="91cb2-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="91cb2-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="91cb2-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="91cb2-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="91cb2-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="91cb2-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="91cb2-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="91cb2-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="91cb2-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="91cb2-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="91cb2-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91cb2-115">Élément parent</span><span class="sxs-lookup"><span data-stu-id="91cb2-115">Parent Element</span></span></th>
<th><span data-ttu-id="91cb2-116">Description</span><span class="sxs-lookup"><span data-stu-id="91cb2-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91cb2-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="91cb2-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="91cb2-118">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="91cb2-118">Modem DM configuration profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91cb2-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="91cb2-119"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="91cb2-120">Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</span><span class="sxs-lookup"><span data-stu-id="91cb2-120">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="91cb2-121">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="91cb2-121">This element is new for v4.</span></span> <span data-ttu-id="91cb2-122">Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable.</span><span class="sxs-lookup"><span data-stu-id="91cb2-122">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="91cb2-123">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="91cb2-123">This element is optional.</span></span> <span data-ttu-id="91cb2-124">Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</span><span class="sxs-lookup"><span data-stu-id="91cb2-124">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="91cb2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91cb2-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91cb2-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="91cb2-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



