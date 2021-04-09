---
description: Le roamApplicabilityType décrit les conditions d’itinérance pour lesquelles un profil itinérant s’applique.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d81214ab5a44dcac60bb5e1a6accc81b0d0418
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862505"
---
# <a name="span-idwwan_profile_v4simpletype_roamapplicabilitytypespanroamapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_roamApplicabilityType"></span>Type simple roamApplicabilityType

Le roamApplicabilityType décrit les conditions d’itinérance pour lesquelles un profil itinérant s’applique.

Il s’agit d’un attribut plus expressif que [**roamControlType**](simpletype-roamcontroltype.md), et un profil doit utiliser **roamControlType** ou **roamApplicabilityType**, mais pas les deux. (Si un profil utilise les deux, les deux sont appliqués. Le résultat est l’intersection des deux.)

Utilisez cet attribut pour faire la distinction entre plusieurs profils avec des conditions d’itinérance disjointes, afin de spécifier des attributs de profil différents pour, par exemple, à l’emplacement d’hébergement et l’itinérance.

Il existe trois États d’inscription personnels/itinérants possibles :

-   Page d’hébergement : inscrit sur le réseau privé
-   Partenaire : inscrit sur un réseau étroitement affilié au réseau privé
-   Non partenaire : inscrit sur un réseau qui n’est pas étroitement affilié au réseau privé

La signification précise de « partenaire » varie en fonction du réseau, mais il représente une relation plus étroite avec des tarifs plus favorables qu’un partenaire non partenaire. Cela peut être le cas si un opérateur basé sur une région a une organisation d’entreprise pour utiliser le réseau d’accès radio d’un autre opérateur en dehors de sa zone d’hébergement. Il peut également représenter la différence entre l’itinérance au sein d’une région (par exemple, l’UE) et l’extérieur.

``` syntax
<xs:simpleType name="roamApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="NonPartnerOnly"
         />
        <xs:enumeration
            value="PartnerOnly"
         />
        <xs:enumeration
            value="HomeOnly"
         />
        <xs:enumeration
            value="HomeAndPartner"
         />
        <xs:enumeration
            value="PartnerAndNonpartner"
         />
        <xs:enumeration
            value="AllRoaming"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **roamApplicabilityType** définit les valeurs suivantes.

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
<td>NonPartnerOnly</td>
<td><p>Ce profil est utilisé uniquement lors de l’itinérance sur un réseau non partenaire</p></td>
</tr>
<tr class="even">
<td>PartnerOnly</td>
<td><p>Ce profil est utilisé uniquement lors de l’itinérance sur un réseau partenaire</p></td>
</tr>
<tr class="odd">
<td>HomeOnly</td>
<td><p>Ce profil est utilisé uniquement sur le réseau privé.</p></td>
</tr>
<tr class="even">
<td>HomeAndPartner</td>
<td><p>Ce profil est utilisé uniquement quand vous êtes au bureau ou sur un réseau partenaire</p></td>
</tr>
<tr class="odd">
<td>PartnerAndNonpartner</td>
<td><p>Ce profil est utilisé en cas de non-démarrage (itinérance sur n’importe quel réseau)</p></td>
</tr>
<tr class="even">
<td>AllRoaming</td>
<td><p>Ce profil est utilisé sur tous les réseaux</p></td>
</tr>
</tbody>
</table>

 

 



