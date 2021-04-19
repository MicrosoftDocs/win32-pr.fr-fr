---
description: ModemDMConfigProfile \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec57fbe0bbcb4c633ddb8485f048ce4230e0ca5
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106533293"
---
# <a name="span-idwwan_profile_v4element_1_iptypespanmodemdmconfigprofileiptype-v4"></a><span data-ttu-id="7f127-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile \/ ... \/ IPType (v4)</span><span class="sxs-lookup"><span data-stu-id="7f127-103"><span id="WWAN_profile_v4.element_1_IPType"></span>ModemDMConfigProfile\/...\/IPType (v4)</span></span>

<span data-ttu-id="7f127-104">Spécifie le type d’IP à utiliser sur cette connexion de données.</span><span class="sxs-lookup"><span data-stu-id="7f127-104">Specifies the IP type to be used on this data connection.</span></span>

<span data-ttu-id="7f127-105">Cet élément est une nouveauté de v4 du schéma.</span><span class="sxs-lookup"><span data-stu-id="7f127-105">This element is new in v4 of the schema.</span></span> <span data-ttu-id="7f127-106">L’élément peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7f127-106">The element can have one of the following values.</span></span>

| <span data-ttu-id="7f127-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f127-107">Value</span></span>   | <span data-ttu-id="7f127-108">Signification</span><span class="sxs-lookup"><span data-stu-id="7f127-108">Meaning</span></span>                                       |
|---------|-----------------------------------------------|
| <span data-ttu-id="7f127-109">Default</span><span class="sxs-lookup"><span data-stu-id="7f127-109">Default</span></span> | <span data-ttu-id="7f127-110">Le type d’adresse IP doit être choisi par la ou les couches inférieures</span><span class="sxs-lookup"><span data-stu-id="7f127-110">IP type is to be picked by lower layer(s)</span></span>     |
| <span data-ttu-id="7f127-111">IPv4</span><span class="sxs-lookup"><span data-stu-id="7f127-111">IPv4</span></span>    | <span data-ttu-id="7f127-112">Utiliser IPv4</span><span class="sxs-lookup"><span data-stu-id="7f127-112">Use IPv4</span></span>                                      |
| <span data-ttu-id="7f127-113">IPv6</span><span class="sxs-lookup"><span data-stu-id="7f127-113">IPv6</span></span>    | <span data-ttu-id="7f127-114">Utiliser IPv6</span><span class="sxs-lookup"><span data-stu-id="7f127-114">Use IPv6</span></span>                                      |
| <span data-ttu-id="7f127-115">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="7f127-115">IPv4v6</span></span>  | <span data-ttu-id="7f127-116">Utilisez IPv4 et/ou IPv6, comme disponible.</span><span class="sxs-lookup"><span data-stu-id="7f127-116">Use IPv4 and/or IPv6, as available.</span></span>           |
| <span data-ttu-id="7f127-117">XLAT</span><span class="sxs-lookup"><span data-stu-id="7f127-117">XLAT</span></span>    | <span data-ttu-id="7f127-118">Utiliser 464XLAT pour transférer des réseaux IPv4 sur des réseaux IPv6</span><span class="sxs-lookup"><span data-stu-id="7f127-118">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span> |

 

## <a name="element-hierarchy"></a><span data-ttu-id="7f127-119">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="7f127-119">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a><span data-ttu-id="7f127-120">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f127-120">Syntax</span></span>

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="7f127-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7f127-121"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="7f127-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="7f127-122"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="7f127-123">Aucun</span><span class="sxs-lookup"><span data-stu-id="7f127-123">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="7f127-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7f127-124"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="7f127-125">Aucun</span><span class="sxs-lookup"><span data-stu-id="7f127-125">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="7f127-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7f127-126"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f127-127">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7f127-127">Parent Element</span></span></th>
<th><span data-ttu-id="7f127-128">Description</span><span class="sxs-lookup"><span data-stu-id="7f127-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f127-129"><a href="element-1-context.md">Contexte</a></span><span class="sxs-lookup"><span data-stu-id="7f127-129"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="7f127-130">Spécifie les paramètres requis pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="7f127-130">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="7f127-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f127-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f127-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f127-132">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



