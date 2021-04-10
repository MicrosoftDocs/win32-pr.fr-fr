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
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113454"
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
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
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

 

 




