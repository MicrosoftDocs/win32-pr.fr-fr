---
description: PurposeGroupGuid
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroupGuid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d772a79d1802c99cde571abc1c665c73ddd06c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476075"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid

Représente un profil dans un PurposeGroup de profils.

Les profils sont spécifiés par leur valeur [**guidType**](simpletype-guidtype.md) .

Quatre valeurs GUID sont définies, comme indiqué dans le tableau suivant.

| Groupe d’objectifs | GUID                                 |
|---------------|--------------------------------------|
| Internet      | 3E5545D2-1137-4DC8-A198-33F1C657515F |
| mms           | 53E2C5D3-D13C-4068-AA38-9C48FF2E55A8 |
| IMS           | 474D66ED-0E4B-476B-A455-19BB1239ED13 |
| SUPL          | 6D42669F-52A9-408E-9493-1071DCC437BD |

 

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a>Syntax

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Liste facultative de groupes de profils, où chaque groupe comprend des profils utilisés dans un but commun.</p><p>Cet élément est une nouveauté pour v4 du schéma.</p><p>Un profil peut être listé dans plusieurs groupes.</p> | 


 

## <a name="requirements"></a>Configuration requise


| | | <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



