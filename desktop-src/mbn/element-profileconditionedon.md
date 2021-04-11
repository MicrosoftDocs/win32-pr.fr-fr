---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112911"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

Spécifie les conditions qui doivent être satisfaites pour qu’un profil soit applicable.

Cet élément est une nouveauté pour v4. Elle vous permet de spécifier plusieurs profils qui s’appliquent dans différentes conditions, et pour que le profil approprié soit utilisé automatiquement lorsqu’il est applicable. Cet élément est facultatif. Si vous ne le spécifiez pas, le profil est toujours applicable en ce qui concerne les conditions indiquées.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Syntaxe

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
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
<td><a href="element-cellularclass.md">CellularClass</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsque la classe cellulaire actuelle est celle spécifiée. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsque la IMSI actuelle utilisée dans le ICCID est celle spécifiée. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">IwlanApplicability</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsqu’il est connecté à un réseau IWLAN. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol). La valeur de cet élément doit être une valeur <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> valide.</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">RATApplicability</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsque le type de RAT est celui spécifié. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol).</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">RoamApplicability</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsque la condition d’itinérance actuelle est celle spécifiée. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol). La valeur de cet élément doit être une valeur <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valide.</p></td>
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
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent. Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</p>
<p>Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement. Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</p></td>
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

 

 



