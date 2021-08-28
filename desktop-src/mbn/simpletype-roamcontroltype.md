---
description: Décrit comment le profil contrôle l’itinérance.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamControlType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamControlType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19243625c07afae49011638a37734a5515e626d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480235"
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


| Valeur | Description | 
|-------|-------------|
| AllRoamAllowed | <p>L’itinérance est autorisée sur les réseaux partenaires et non-partenaires.</p> | 
| PartnerRoamAllowed | <p>L’itinérance est autorisée uniquement sur les réseaux partenaires.</p> | 
| NoRoamAllowed | <p>Aucune itinérance n’est autorisée.</p> | 


 

 



