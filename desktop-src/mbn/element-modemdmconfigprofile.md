---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543658"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Profil de configuration DM du modem.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

**<ModemDMConfigProfile>**

## <a name="syntax"></a>Syntaxe

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a>Clé

`?`   facultatif (zéro ou un)

`*`   facultatif (zéro, un ou plusieurs)

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
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Spécifie si le profil est activé de manière administrative. Il s’agit d’un nouvel élément pour v4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Spécifie si le profil est contrôlé par un itinérance administrative. Cet élément est une nouveauté pour v4. La valeur de cet élément est une valeur <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Il s’agit d’un élément facultatif ; Si aucune valeur n’est spécifiée, <strong>AllRoamAllowed</strong> est la valeur par défaut.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>ID APN associé à ce profil. Cet élément est une nouveauté de V4 et il est facultatif.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Contexte</a></td>
<td><p>Spécifie les paramètres requis pour établir une connexion de données.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Nom</a></td>
<td><p>Nom du profil. Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nom</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>ID de connexion OEM pour la configuration DM du modem.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (dans ModemDMConfigProfile)</a></td>
<td><p>Spécifie comment ce profil de DM de modem a été créé.</p>
<p>Cette valeur est utilisée pour déterminer si un utilisateur peut supprimer le profil. Les utilisateurs peuvent uniquement supprimer des profils <strong>UserProvisioned</strong> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Spécifie que ce profil est actif uniquement lorsque la condition d’itinérance actuelle est celle spécifiée. Dans le cas contraire, le profil n’est pas applicable et ne peut pas être utilisé pour activer un contexte PDP (Packet Data Protocol). La valeur de cet élément doit être une valeur <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valide.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>Numéro de identifcation SIM pour les appareils GSM. Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents

Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.

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

 

 



