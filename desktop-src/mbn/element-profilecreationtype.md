---
description: ProfileCreationType (dans MBNProfileExt)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (dans MBNProfileExt)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56e09a18721bfa7d5f33d8e7511122f3d731f4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751956"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span data-ttu-id="16bcf-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (dans MBNProfileExt)</span><span class="sxs-lookup"><span data-stu-id="16bcf-103"><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (in MBNProfileExt)</span></span>

<span data-ttu-id="16bcf-104">Spécifie le créateur du profil.</span><span class="sxs-lookup"><span data-stu-id="16bcf-104">Specifies the creator of the profile.</span></span>

<span data-ttu-id="16bcf-105">Pour plus d’informations sur cet élément, consultez la documentation de l’élément [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="16bcf-105">For more information about this element, see the documentation for the v1 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="16bcf-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="16bcf-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="16bcf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16bcf-107">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="16bcf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="16bcf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="16bcf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="16bcf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="16bcf-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="16bcf-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="16bcf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="16bcf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="16bcf-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="16bcf-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="16bcf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="16bcf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16bcf-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="16bcf-114">Parent Element</span></span></th>
<th><span data-ttu-id="16bcf-115">Description</span><span class="sxs-lookup"><span data-stu-id="16bcf-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16bcf-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="16bcf-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="16bcf-117">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="16bcf-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="16bcf-118">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="16bcf-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="16bcf-119">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="16bcf-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="16bcf-120">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="16bcf-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="16bcf-121">Éléments apparentés</span><span class="sxs-lookup"><span data-stu-id="16bcf-121">Related elements</span></span>

<span data-ttu-id="16bcf-122">Les éléments suivants portent le même nom que celui-ci, mais ils ont un contenu ou des attributs différents :</span><span class="sxs-lookup"><span data-stu-id="16bcf-122">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="16bcf-123">**[ProfileCreationType (dans ModemDMConfigProfile)](element-1-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="16bcf-123">**[ProfileCreationType (in ModemDMConfigProfile)](element-1-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="16bcf-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16bcf-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16bcf-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="16bcf-125">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
