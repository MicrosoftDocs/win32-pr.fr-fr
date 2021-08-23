---
description: Spécifie le nombre de tentatives de pré-authentification pour essayer sur les points d’accès voisins.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Élément preAuthThrottle (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8bc310d19126a0e4bc9a7e6abf2a6ae1d0eb917cb5f425796d10bee66ea6ebed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064599"
---
# <a name="preauththrottle-security-element"></a>Élément preAuthThrottle (Security)

L’élément preAuthThrottle (Security) spécifie le nombre de tentatives de pré-authentification pour essayer sur les points d’accès voisins. Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ». Si **PMKCacheMode** est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.

``` syntax
<xs:element name="preAuthThrottle"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**caution**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**sécurité (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




