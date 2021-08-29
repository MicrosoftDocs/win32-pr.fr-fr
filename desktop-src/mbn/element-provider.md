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
ms.openlocfilehash: badca53e9b92e647172c35662db81742e3555645
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886061"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span id="WWAN_profile_v4.element_Provider"></span>Fournisseur

Spécifie un fournisseur de réseau préféré dans une liste de fournisseurs à utiliser lors de l’itinérance.

La valeur de cet élément est une instance du type complexe v1 [**ProviderType**](./schema-providertype-complextype.md) .

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;DataRoamingPartners&gt;](element-dataroamingpartners.md)  
**&lt;Fournisseur&gt;**

## <a name="syntax"></a>Syntaxe

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Spécifie une liste de fournisseurs de réseau préférés lors de l’itinérance.</p><p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</p> | 


 

## <a name="requirements"></a>Spécifications


| | | <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
