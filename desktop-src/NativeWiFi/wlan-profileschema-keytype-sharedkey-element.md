---
description: Indique si la clé partagée sera une clé réseau ou une phrase secrète.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: KeyType (sharedKey), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531708"
---
# <a name="keytype-sharedkey-element"></a>KeyType (sharedKey), élément

L’élément KeyType (sharedKey) indique si la clé partagée sera une clé réseau ou une phrase secrète.

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par l’élément [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Notes

Lorsque l’élément de [**chiffrement**](wlan-profileschema-encryption-authencryption-element.md) a la valeur WEP, **KeyType** doit être défini sur **networkKey**.

## <a name="examples"></a>Exemples

Pour afficher des exemples de profils qui utilisent l’élément **KeyType** , consultez exemple de [profil de non-diffusion](non-broadcast-profile-sample.md), exemple de [Profil WPA-Personnel](wpa-personal-profile-sample.md)et exemple de profil [WPA2-Personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sharedKey (sécurité)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




