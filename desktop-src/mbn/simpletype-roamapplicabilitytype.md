---
description: Le roamApplicabilityType décrit les conditions d’itinérance pour lesquelles un profil itinérant s’applique.
MS-HAID: WWAN\_profile\_v4.simpleType\_roamApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple roamApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2ce8f24e0987d5e8463838b33d4f2f2cf859da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415849"
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


| Valeur | Description | 
|-------|-------------|
| NonPartnerOnly | <p>Ce profil est utilisé uniquement lors de l’itinérance sur un réseau non partenaire</p> | 
| PartnerOnly | <p>Ce profil est utilisé uniquement lors de l’itinérance sur un réseau partenaire</p> | 
| HomeOnly | <p>Ce profil est utilisé uniquement sur le réseau privé.</p> | 
| HomeAndPartner | <p>Ce profil est utilisé uniquement quand vous êtes au bureau ou sur un réseau partenaire</p> | 
| PartnerAndNonpartner | <p>Ce profil est utilisé en cas de non-démarrage (itinérance sur n’importe quel réseau)</p> | 
| AllRoaming | <p>Ce profil est utilisé sur tous les réseaux</p> | 


 

 



