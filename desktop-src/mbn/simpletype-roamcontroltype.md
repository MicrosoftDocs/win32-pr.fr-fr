---
description: Décrit comment le profil contrôle l’itinérance.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911e379773e7d8eabfb7a1524b1a21ba16718a53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514199"
---
# <a name="span-idwwan_profile_v4simpletype_roamcontroltypespanroamcontroltype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamControlType"></span>Type simple roamControlType

Décrit comment le profil contrôle l’itinérance.

Il existe deux États d’inscription itinérants possibles :

-   Partenaire : inscrit sur un réseau étroitement affilié au réseau privé
-   Non partenaire : inscrit sur un réseau qui n’est pas étroitement affilié au réseau privé

La signification précise de « partenaire » varie en fonction du réseau, mais il représente une relation plus étroite avec des tarifs plus favorables qu’un partenaire non partenaire. Cela peut être le cas si un opérateur basé sur une région a une organisation d’entreprise pour utiliser le réseau d’accès radio d’un autre opérateur en dehors de sa zone d’hébergement. Il peut également représenter la différence entre l’itinérance au sein d’une région (par exemple, l’UE) et l’extérieur.

Notez que [**roamApplicabilityType**](simpletype-roamapplicabilitytype.md) est un attribut plus expressif que **roamControlType**, et qu’un profil doit utiliser **roamControlType** ou **roamApplicabilityType**, mais pas les deux. (Si un profil utilise les deux, les deux sont appliqués. Le résultat est l’intersection des deux.)

``` syntax
<xs:simpleType name="roamControlType">
    <xs:restriction>
        <xs:enumeration
            value="AllRoamAllowed"
         />
        <xs:enumeration
            value="PartnerRoamAllowed"
         />
        <xs:enumeration
            value="NoRoamAllowed"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **roamControlType** définit les valeurs suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllRoamAllowed</td>
<td><p>L’itinérance est autorisée sur les réseaux partenaires et non-partenaires.</p></td>
</tr>
<tr class="even">
<td>PartnerRoamAllowed</td>
<td><p>L’itinérance est autorisée uniquement sur les réseaux partenaires.</p></td>
</tr>
<tr class="odd">
<td>NoRoamAllowed</td>
<td><p>Aucune itinérance n’est autorisée.</p></td>
</tr>
</tbody>
</table>

 

 



