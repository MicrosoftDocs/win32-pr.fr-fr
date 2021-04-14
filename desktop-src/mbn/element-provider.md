---
description: Fournisseur
MS-HAID: WWAN\_profile\_v4.element\_Provider
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Fournisseur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a701c4dd-967f-4f03-ada4-d34059f5a1e4
api_name:
- Provider
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7b4658e51f6f137795a935121dc90c047cf047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484833"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span data-ttu-id="418cf-103"><span id="WWAN_profile_v4.element_Provider"></span>Moteur</span><span class="sxs-lookup"><span data-stu-id="418cf-103"><span id="WWAN_profile_v4.element_Provider"></span>Provider</span></span>

<span data-ttu-id="418cf-104">Spécifie un fournisseur de réseau préféré dans une liste de fournisseurs à utiliser lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="418cf-104">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span>

<span data-ttu-id="418cf-105">La valeur de cet élément est une instance du type complexe v1 [**ProviderType**](./schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="418cf-105">The value of this element is an instance of the v1 [**providerType**](./schema-providertype-complextype.md) complex type.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="418cf-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="418cf-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<DataRoamingPartners>](element-dataroamingpartners.md)  
**<Provider>**

## <a name="syntax"></a><span data-ttu-id="418cf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="418cf-107">Syntax</span></span>

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="418cf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="418cf-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="418cf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="418cf-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="418cf-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="418cf-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="418cf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="418cf-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="418cf-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="418cf-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="418cf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="418cf-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="418cf-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="418cf-114">Parent Element</span></span></th>
<th><span data-ttu-id="418cf-115">Description</span><span class="sxs-lookup"><span data-stu-id="418cf-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="418cf-116"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="418cf-116"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="418cf-117">Spécifie une liste de fournisseurs de réseau préférés lors de l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="418cf-117">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="418cf-118">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="418cf-118">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="418cf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="418cf-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="418cf-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="418cf-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
