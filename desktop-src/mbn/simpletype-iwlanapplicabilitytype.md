---
description: Énumération qui décrit le type de connexion réseau où un profil est applicable.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529ae39c2b0e137825e7a80d41c43203b0a27de7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478955"
---
# <a name="span-idwwan_profile_v4simpletype_iwlanapplicabilitytypespaniwlanapplicabilitytype-simple-type"></a><span id="WWAN_profile_v4.simpleType_iwlanApplicabilityType"></span>Type simple iwlanApplicabilityType

Énumération qui décrit le type de connexion réseau où un profil est applicable.

``` syntax
<xs:simpleType name="iwlanApplicabilityType">
    <xs:restriction
        base="token"
    >
        <xs:enumeration
            value="CellularOnly"
         />
        <xs:enumeration
            value="CellularAndIwlan"
         />
        <xs:enumeration
            value="IwlanOnly"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **iwlanApplicabilityType** définit les valeurs suivantes.


| Valeur | Description | 
|-------|-------------|
| CellularOnly | <p>Le profil est valide uniquement pour les connexions au réseau cellulaire.</p> | 
| CellularAndIwlan | <p>Le profil est valide pour les connexions mobiles ou Wi-Fi déchargées.</p> | 
| IwlanOnly | <p>Le profil est valide uniquement pour les connexions Wi-Fi déchargées.</p> | 


 

 



