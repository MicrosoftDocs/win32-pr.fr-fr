---
description: ProfileCreationType (dans ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (dans ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29867412bbadc8041bcf864a9575b0fc6001a499
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479955"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (dans ModemDMConfigProfile)

Spécifie comment ce profil de DM de modem a été créé.

Cette valeur est utilisée pour déterminer si un utilisateur peut supprimer le profil. Les utilisateurs peuvent uniquement supprimer des profils **UserProvisioned** .

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a> | <p>Profil de configuration DM du modem.</p> | 


 

## <a name="related-elements"></a>Éléments apparentés

Les éléments suivants portent le même nom que celui-ci, mais ils ont un contenu ou des attributs différents :

-   **[ProfileCreationType (dans MBNProfileExt)](element-profilecreationtype.md)**

## <a name="requirements"></a>Configuration requise


| | | <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



