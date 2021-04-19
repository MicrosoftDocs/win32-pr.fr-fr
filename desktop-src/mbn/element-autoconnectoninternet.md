---
description: AutoConnectOnInternet
MS-HAID: WWAN\_profile\_v4.element\_AutoConnectOnInternet
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AutoConnectOnInternet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e42d42285ba97e8415fdd1c8e8ddddb329338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515676"
---
# <a name="span-idwwan_profile_v4element_autoconnectoninternetspanautoconnectoninternet"></a><span data-ttu-id="3fe9e-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet</span><span class="sxs-lookup"><span data-stu-id="3fe9e-103"><span id="WWAN_profile_v4.element_AutoConnectOnInternet"></span>AutoConnectOnInternet</span></span>

<span data-ttu-id="3fe9e-104">Spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-104">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="3fe9e-105">Pour plus d’informations, consultez la documentation de l’élément [**AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-105">For more information, see the documentation for the v1 [**AutoConnectOnInternet**](./schema-autoconnectoninternet-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3fe9e-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="3fe9e-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<AutoConnectOnInternet>**

## <a name="syntax"></a><span data-ttu-id="3fe9e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fe9e-107">Syntax</span></span>

``` syntax
<AutoConnectOnInternet>

  boolean

</AutoConnectOnInternet>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3fe9e-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="3fe9e-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3fe9e-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="3fe9e-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3fe9e-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="3fe9e-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3fe9e-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3fe9e-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3fe9e-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="3fe9e-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3fe9e-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3fe9e-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fe9e-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3fe9e-114">Parent Element</span></span></th>
<th><span data-ttu-id="3fe9e-115">Description</span><span class="sxs-lookup"><span data-stu-id="3fe9e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3fe9e-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="3fe9e-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="3fe9e-117">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="3fe9e-118">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="3fe9e-119">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="3fe9e-120">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="3fe9e-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3fe9e-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fe9e-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fe9e-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3fe9e-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
