---
description: Spécifie quand l’authentification unique est effectuée.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Élément type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a8a395a5cdbd21bd33012e624f069d9447204cc96ffd2996a138ebf5d65f7bb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800729"
---
# <a name="type-singlesignon-element"></a>Élément type (singleSignOn)

L’élément type (singleSignOn) spécifie quand l’authentification unique est effectuée. Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session. Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **type** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




