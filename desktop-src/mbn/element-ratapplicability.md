---
description: RATApplicability
MS-HAID: WWAN\_profile\_v4.element\_RATApplicability
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RATApplicability
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df188ec628961aed8aeb5d68e3b9b3f7852e7fdd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986852"
---
# <a name="span-idwwan_profile_v4element_ratapplicabilityspanratapplicability"></a><span id="WWAN_profile_v4.element_RATApplicability"></span>RATApplicability

Spécifie que ce profil est actif uniquement lorsque le type de RAT est celui spécifié. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ProfileConditionedOn&gt;](element-profileconditionedon.md)  
**&lt;RATApplicability&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<RATApplicability>

  "LTE_eHRPD" | "3GPP_LEGACY"

</RATApplicability>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.</p><p>Cet élément est une nouveauté pour v4. Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable. Cet élément est facultatif. Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.</p> | 


 

## <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



