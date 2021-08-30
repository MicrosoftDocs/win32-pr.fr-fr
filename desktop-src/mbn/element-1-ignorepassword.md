---
description: ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bb5f81d5c2fe52cafec8877dfcfb84bc68f51d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478255"
---
# <a name="span-idwwan_profile_v4element_1_ignorepasswordspanmodemdmconfigprofileignorepassword-v4"></a><span id="WWAN_profile_v4.element_1_IgnorePassword"></span>ModemDMConfigProfile \/ ... \/ IgnorePassword (v4)

Spécifie la manière dont les mots de passe sont gérés lors de la mise à niveau des profils.

Si la valeur est **true** et qu’un profil portant le même nom existe au moment de l’opération de mise à jour, le mot de passe de ce profil est pris et stocké dans le nouveau profil.

Pour plus d’informations, consultez la documentation de l’élément [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) v1.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a>Syntax

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents


| Élément parent | Description | 
|----------------|-------------|
| <a href="element-1-userlogoncred.md">UserLogonCred</a> | <p>Informations d’identification d’ouverture de session pour une connexion.</p> | 


 

## <a name="requirements"></a>Configuration requise


| | | <p>Espace de noms</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
