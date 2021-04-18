---
description: MBNProfileExt \/ ... \/ UserLogonCred (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 12a65d91-1917-49d4-9b58-68c60464c857
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f6999763e82051fa30af6109c3a04ae8dc65f77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543089"
---
# <a name="span-idwwan_profile_v4element_userlogoncredspanmbnprofileextuserlogoncred-v4"></a><span id="WWAN_profile_v4.element_UserLogonCred"></span>MBNProfileExt \/ ... \/ UserLogonCred (v4)

Informations d’identification d’ouverture de session pour une connexion.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a>Syntaxe

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a>Clé

`?`   facultatif (zéro ou un)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément enfant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-ignorepassword.md">IgnorePassword</a></td>
<td><p>Spécifie la manière dont les mots de passe sont gérés lors de la mise à niveau des profils.</p>
<p>Si la valeur est <strong>true</strong> et qu’un profil portant le même nom existe au moment de l’opération de mise à jour, le mot de passe de ce profil est pris et stocké dans le nouveau profil.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-password.md">Mot de passe</a></td>
<td><p>Spécifie le mot de passe utilisé pour authentifier un utilisateur.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-password-userlogoncred-element.md"><strong>mot de passe</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-username.md">UserName</a></td>
<td><p>Nom d’utilisateur à utiliser pour l’ouverture de session.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-username-userlogoncred-element.md"><strong>nom d’utilisateur</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément parent</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-context.md">Contexte</a></td>
<td><p>Spécifie les paramètres requis pour établir une connexion de données.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espace de noms</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



