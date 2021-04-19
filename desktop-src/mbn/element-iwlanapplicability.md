---
description: IwlanApplicability
MS-HAID: WWAN\_profile\_v4.element\_IwlanApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IwlanApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6b8b0376f2ee882a57e4c71e392fb7b02f6eeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517265"
---
# <a name="span-idwwan_profile_v4element_iwlanapplicabilityspaniwlanapplicability"></a><span data-ttu-id="f8530-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span><span class="sxs-lookup"><span data-stu-id="f8530-103"><span id="WWAN_profile_v4.element_IwlanApplicability"></span>IwlanApplicability</span></span>

<span data-ttu-id="f8530-104">Spécifie que ce profil est actif uniquement lorsqu’il est connecté à un réseau IWLAN.</span><span class="sxs-lookup"><span data-stu-id="f8530-104">Specifies that this profile is active only when connected to an IWLAN network.</span></span> <span data-ttu-id="f8530-105">Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="f8530-105">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="f8530-106">La valeur de cet élément doit être une valeur [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) valide.</span><span class="sxs-lookup"><span data-stu-id="f8530-106">The value of this element must be a valid [**iwlanApplicabilityType**](simpletype-iwlanapplicabilitytype.md) value.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f8530-107">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="f8530-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<ProfileConditionedOn>](element-profileconditionedon.md)  
**<IwlanApplicability>**

## <a name="syntax"></a><span data-ttu-id="f8530-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8530-108">Syntax</span></span>

``` syntax
<IwlanApplicability>

  "CellularOnly" | "CellularAndIwlan" | "IwlanOnly"

</IwlanApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f8530-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f8530-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f8530-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="f8530-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f8530-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8530-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f8530-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f8530-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f8530-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8530-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f8530-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f8530-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8530-115">Élément parent</span><span class="sxs-lookup"><span data-stu-id="f8530-115">Parent Element</span></span></th>
<th><span data-ttu-id="f8530-116">Description</span><span class="sxs-lookup"><span data-stu-id="f8530-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8530-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="f8530-117"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="f8530-118">Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</span><span class="sxs-lookup"><span data-stu-id="f8530-118">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="f8530-119">Cet élément est une nouveauté pour v4.</span><span class="sxs-lookup"><span data-stu-id="f8530-119">This element is new for v4.</span></span> <span data-ttu-id="f8530-120">Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable.</span><span class="sxs-lookup"><span data-stu-id="f8530-120">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="f8530-121">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f8530-121">This element is optional.</span></span> <span data-ttu-id="f8530-122">Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</span><span class="sxs-lookup"><span data-stu-id="f8530-122">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="f8530-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8530-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8530-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8530-124">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



