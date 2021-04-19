---
description: IsExclusiveToOther
MS-HAID: WWAN\_profile\_v4.element\_IsExclusiveToOther
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsExclusiveToOther
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a948ad9b6a457f74e98eab745d851bdd2399c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516451"
---
# <a name="span-idwwan_profile_v4element_isexclusivetootherspanisexclusivetoother"></a><span data-ttu-id="b9169-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span><span class="sxs-lookup"><span data-stu-id="b9169-103"><span id="WWAN_profile_v4.element_IsExclusiveToOther"></span>IsExclusiveToOther</span></span>

<span data-ttu-id="b9169-104">Spécifie que ce profil est exclusif à d’autres profils du ou des mêmes jeux de profils. Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="b9169-104">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="b9169-105">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="b9169-105">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<IsExclusiveToOther>**

## <a name="syntax"></a><span data-ttu-id="b9169-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9169-106">Syntax</span></span>

``` syntax
<IsExclusiveToOther>

  boolean

</IsExclusiveToOther>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="b9169-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b9169-107"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="b9169-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="b9169-108"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="b9169-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9169-109">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="b9169-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9169-110"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="b9169-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="b9169-111">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="b9169-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b9169-112"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b9169-113">Élément parent</span><span class="sxs-lookup"><span data-stu-id="b9169-113">Parent Element</span></span></th>
<th><span data-ttu-id="b9169-114">Description</span><span class="sxs-lookup"><span data-stu-id="b9169-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b9169-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="b9169-115"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="b9169-116">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="b9169-116">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="b9169-117">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="b9169-117">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="b9169-118">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="b9169-118">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="b9169-119">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="b9169-119">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="b9169-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9169-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9169-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b9169-121">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



