---
description: '\/Contexte ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contexte (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 36007bc1a7aecb25c2b6d61f74dd826e888a314b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118158"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span id="WWAN_profile_v4.element_1_Context"></span>\/Contexte ModemDMConfigProfile (v4)

Spécifie les paramètres requis pour établir une connexion de données.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Syntaxe

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Clé

`?`   facultatif (zéro ou un)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément enfant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-accessstring.md">AccessString</a></td>
<td><p>Identifie l’APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-authprotocol.md">AuthProtocol</a></td>
<td><p>>Spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).</p>
<p>Notez que, dans v4, une nouvelle valeur d’énumération est disponible pour cet élément. La <strong>sélection SELECT</strong> signifie qu’un protocole d’authentification doit être choisi par des couches inférieures.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> v1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-compression.md">Compression</a></td>
<td><p>Spécifie si la compression est utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données.</p>
<p>Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-compression-contexttype-element.md"><strong>compression</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-iptype.md">IPType</a></td>
<td><p>Spécifie le type d’IP à utiliser sur cette connexion de données.</p>
<p>Cet élément est une nouveauté de v4 du schéma. L’élément peut avoir l’une des valeurs suivantes.</p>
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Default</td>
<td>Le type d’adresse IP doit être choisi par la ou les couches inférieures</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>Utiliser IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>Utiliser IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Utilisez IPv4 et/ou IPv6, comme disponible.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Utiliser 464XLAT pour transférer des réseaux IPv4 sur des réseaux IPv6</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-1-userlogoncred.md">UserLogonCred</a></td>
<td><p>Informations d’identification d’ouverture de session pour une connexion.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Élément parent</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent. Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</p>
<p>Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement. Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Profil de configuration DM du modem.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Spécifications

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espace de noms</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



