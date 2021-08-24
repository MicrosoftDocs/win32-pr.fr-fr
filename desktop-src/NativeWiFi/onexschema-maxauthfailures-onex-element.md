---
description: Spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Élément maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9cb48479b2fe26ecb2667812cc6ee2048226c0665c25b12e25e8c7edbc35dac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800779"
---
# <a name="maxauthfailures-onex-element"></a>Élément maxAuthFailures (OneX)

L’élément maxAuthFailures (OneX) spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.

Cet élément est facultatif. Quand maxAuthFailures n’est pas spécifié dans un profil, la valeur 1 est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **maxAuthFailures** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

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

 

 




