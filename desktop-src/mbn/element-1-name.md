---
description: '\/Nom ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Name
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Nom (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5db3565-db0a-4e6d-a0c5-7e9b3d006d5d
api_name:
- Name
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 40fc710649d5e1cb87f69d8358ba5706492b6c5f
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106528850"
---
# <a name="span-idwwan_profile_v4element_1_namespanmodemdmconfigprofilename-v4"></a><span data-ttu-id="3e295-103"><span id="WWAN_profile_v4.element_1_Name"></span>\/Nom ModemDMConfigProfile (v4)</span><span class="sxs-lookup"><span data-stu-id="3e295-103"><span id="WWAN_profile_v4.element_1_Name"></span>ModemDMConfigProfile\/Name (v4)</span></span>

<span data-ttu-id="3e295-104">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="3e295-104">The name of the profile.</span></span> <span data-ttu-id="3e295-105">Pour plus d’informations, consultez la documentation de l’élément de [**nom**](./schema-name-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="3e295-105">For more information, see the documentation for the v1 [**Name**](./schema-name-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3e295-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="3e295-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Name\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Name\>**

## <a name="syntax"></a><span data-ttu-id="3e295-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e295-107">Syntax</span></span>

``` syntax
<Name>

  nameType

</Name>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3e295-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3e295-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3e295-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="3e295-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3e295-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="3e295-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3e295-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3e295-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3e295-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="3e295-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3e295-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3e295-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e295-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3e295-114">Parent Element</span></span></th>
<th><span data-ttu-id="3e295-115">Description</span><span class="sxs-lookup"><span data-stu-id="3e295-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e295-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3e295-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3e295-117">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="3e295-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3e295-118">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="3e295-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3e295-119">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="3e295-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3e295-120">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="3e295-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e295-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="3e295-121"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="3e295-122">Profil de configuration DM du modem.</span><span class="sxs-lookup"><span data-stu-id="3e295-122">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3e295-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e295-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e295-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3e295-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
