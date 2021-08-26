---
description: PurposeGroups
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroups
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroups
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3b158938e1a41f6ab8d3f1df0cae6a2166bc21c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630935"
---
# <a name="span-idwwan_profile_v4element_purposegroupsspanpurposegroups"></a><span id="WWAN_profile_v4.element_PurposeGroups"></span>PurposeGroups

Liste facultative de groupes de profils, où chaque groupe comprend des profils utilisés dans un but commun.

Cet élément est une nouveauté pour v4 du schéma.

Un profil peut être listé dans plusieurs groupes.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[<MBNProfileExt>](element-mbnprofileext.md)  
**<PurposeGroups>**

## <a name="syntax"></a>Syntax

``` syntax
<PurposeGroups>

  <!-- Child elements -->
  PurposeGroupGuid{1,10}

</PurposeGroups>
```

### <a name="key"></a>Clé :

`{}`   plage spécifique d’occurrences

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
<td><a href="element-purposegroupguid.md">PurposeGroupGuid</a></td>
<td><p>Représente un profil dans un PurposeGroup de profils.</p>
<p>Les profils sont spécifiés par leur valeur <a href="simpletype-guidtype.md"><strong>guidType</strong></a> .</p>
<p>Quatre valeurs GUID sont définies, comme indiqué dans le tableau suivant.</p>
<table>
<thead>
<tr class="header">
<th>Groupe d’objectifs</th>
<th>GUID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Internet</td>
<td>3E5545D2-1137-4DC8-A198-33F1C657515F</td>
</tr>
<tr class="even">
<td>mms</td>
<td>53E2C5D3-D13C-4068-AA38-9C48FF2E55A8</td>
</tr>
<tr class="odd">
<td>IMS</td>
<td>474D66ED-0E4B-476B-A455-19BB1239ED13</td>
</tr>
<tr class="even">
<td>SUPL</td>
<td>6D42669F-52A9-408E-9493-1071DCC437BD</td>
</tr>
</tbody>
</table>
<p> </p></td>
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
</tbody>
</table>

 

## <a name="requirements"></a>Configuration requise

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

 

 



