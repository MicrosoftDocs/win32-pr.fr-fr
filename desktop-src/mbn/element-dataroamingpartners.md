---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6df58bc0765b5254645c45270f8145f5d10d422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515232"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span data-ttu-id="20a12-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span><span class="sxs-lookup"><span data-stu-id="20a12-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span></span>

<span data-ttu-id="20a12-104">Spécifie une liste de fournisseurs de réseau préférés lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="20a12-104">Specifies a list of preferred network providers when roaming.</span></span>

<span data-ttu-id="20a12-105">Pour plus d’informations, consultez la documentation de l’élément [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="20a12-105">For details, see the documentation for the v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="20a12-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="20a12-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a><span data-ttu-id="20a12-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20a12-107">Syntax</span></span>

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a><span data-ttu-id="20a12-108">Clé</span><span class="sxs-lookup"><span data-stu-id="20a12-108">Key</span></span>

<span data-ttu-id="20a12-109">`+`   obligatoire (un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="20a12-109">`+`   required (one or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="20a12-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="20a12-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="20a12-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="20a12-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="20a12-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="20a12-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="20a12-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20a12-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20a12-114">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="20a12-114">Child Element</span></span></th>
<th><span data-ttu-id="20a12-115">Description</span><span class="sxs-lookup"><span data-stu-id="20a12-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20a12-116"><a href="element-provider.md">Fournisseur</a></span><span class="sxs-lookup"><span data-stu-id="20a12-116"><a href="element-provider.md">Provider</a></span></span></td>
<td><p><span data-ttu-id="20a12-117">Spécifie un fournisseur de réseau préféré dans une liste de fournisseurs à utiliser lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="20a12-117">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span></p>
<p><span data-ttu-id="20a12-118">La valeur de cet élément est une instance du type complexe v1 <a href="../mbn/schema-providertype-complextype.md"><strong>ProviderType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="20a12-118">The value of this element is an instance of the v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> complex type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="20a12-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="20a12-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="20a12-120">Élément parent</span><span class="sxs-lookup"><span data-stu-id="20a12-120">Parent Element</span></span></th>
<th><span data-ttu-id="20a12-121">Description</span><span class="sxs-lookup"><span data-stu-id="20a12-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="20a12-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="20a12-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="20a12-123">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="20a12-123">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="20a12-124">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="20a12-124">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="20a12-125">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="20a12-125">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="20a12-126">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="20a12-126">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="20a12-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a12-127">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20a12-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20a12-128">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
