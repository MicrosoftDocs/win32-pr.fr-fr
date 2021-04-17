---
description: Énumération qui décrit le type de connexion réseau où un profil est applicable.
MS-HAID: WWAN\_profile\_v4.simpleType\_iwlanApplicabilityType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Type simple iwlanApplicabilityType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80013fa21574221de24a7fc8309e4459a80ad670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526614"
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
<td>CellularOnly</td>
<td><p>Le profil est valide uniquement pour les connexions au réseau cellulaire.</p></td>
</tr>
<tr class="even">
<td>CellularAndIwlan</td>
<td><p>Le profil est valide pour les connexions mobiles ou Wi-Fi déchargées.</p></td>
</tr>
<tr class="odd">
<td>IwlanOnly</td>
<td><p>Le profil est valide uniquement pour les connexions Wi-Fi déchargées.</p></td>
</tr>
</tbody>
</table>

 

 



