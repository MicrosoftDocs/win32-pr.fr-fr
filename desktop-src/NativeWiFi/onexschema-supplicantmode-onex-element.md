---
description: Spécifie la méthode de transmission utilisée pour EAPOL-Start messages.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Élément supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009444"
---
# <a name="supplicantmode-onex-element"></a>Élément supplicantMode (OneX)

L’élément supplicantMode (OneX) spécifie la méthode de transmission utilisée pour EAPOL-Start messages. Le tableau suivant décrit les valeurs possibles.



| Valeur               | Description                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibitTransmission | Les messages de EAPOL-Start ne sont pas transmis. Valide pour les profils LAN câblés uniquement.                                                                                             |
| includeLearning     | Le client détermine quand envoyer des paquets EAPOL-Start en fonction de la capacité du réseau. Les messages de EAPOL-Start sont envoyés uniquement lorsque cela est nécessaire. Valide pour les profils LAN câblés uniquement. |
| conforme           | EAPOL-Start messages sont transmis comme spécifié par 802.1 X. Valide pour les profils de réseau local câblés et sans fil.                                                             |



 

Cet élément est facultatif. Quand supplicantMode n’est pas spécifié dans un profil, la valeur `compliant` est utilisée pour les profils de réseau local câblés et sans fil.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **supplicantMode** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**802.1x**](onexschema-onex-element.md)
</dt> </dl>

 

 




