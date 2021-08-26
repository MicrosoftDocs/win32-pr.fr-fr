---
description: Contient des informations sur le créateur du profil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Élément ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: ddf3e70607cedbaed45da19651ec73736a54bfafab197e95d2cd634d8e3833f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959839"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Élément ProfileCreationType (MBNProfile)

L’élément **ProfileCreationType (MBNProfile)** contient des informations sur le créateur du profil.

Cet élément peut avoir l’une des valeurs suivantes.



| Valeur                 | Signification                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Ce profil est créé par les informations fournies par l’utilisateur de l’appareil.                                                     |
| "AdminProvisioned"    | Ce profil est créé par les administrateurs informatiques et distribué aux utilisateurs.                                                     |
| "OperatorProvisioned" | Ce profil est créé par un opérateur réseau et distribué aux utilisateurs.                                                    |
| "DeviceProvisioned"   | Ce profil est créé par le service haut débit mobile à l’aide des informations stockées dans le contexte approvisionné par l’appareil. |



 

Cet élément est facultatif.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **ProfileCreationType** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




