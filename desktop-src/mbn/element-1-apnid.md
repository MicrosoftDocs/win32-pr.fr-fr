---
description: ModemDMConfigProfile \/ ApnID (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_ApnID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ApnID (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3838a632359fcdf7bc32004103f6f90163d988
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106537741"
---
# <a name="span-idwwan_profile_v4element_1_apnidspanmodemdmconfigprofileapnid-v4"></a><span data-ttu-id="ff159-103"><span id="WWAN_profile_v4.element_1_ApnID"></span>ModemDMConfigProfile \/ ApnID (v4)</span><span class="sxs-lookup"><span data-stu-id="ff159-103"><span id="WWAN_profile_v4.element_1_ApnID"></span>ModemDMConfigProfile\/ApnID (v4)</span></span>

<span data-ttu-id="ff159-104">ID APN associé à ce profil. Cet élément est une nouveauté de V4 et il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="ff159-104">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ff159-105">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="ff159-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<ApnID\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<ApnID\>**

## <a name="syntax"></a><span data-ttu-id="ff159-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff159-106">Syntax</span></span>

``` syntax
<ApnID>

  decimal

</ApnID>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ff159-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ff159-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ff159-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="ff159-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ff159-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="ff159-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ff159-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff159-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="ff159-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="ff159-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ff159-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ff159-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff159-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="ff159-113">Parent Element</span></span></th>
<th><span data-ttu-id="ff159-114">Description</span><span class="sxs-lookup"><span data-stu-id="ff159-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff159-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="ff159-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="ff159-116">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="ff159-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="ff159-117">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="ff159-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="ff159-118">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="ff159-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="ff159-119">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="ff159-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff159-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="ff159-120"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="ff159-121">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="ff159-121">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="ff159-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff159-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff159-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ff159-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



