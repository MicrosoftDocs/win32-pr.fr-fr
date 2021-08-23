---
description: Spécifie le nombre maximal de messages EAPOL-Start envoyés.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Élément maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7c50945b8de53b6d058556e3b5c995d3ec17bfdc8f8d55ec3dc2e6e56089b2a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800759"
---
# <a name="maxstart-onex-element"></a>Élément maxStart (OneX)

L’élément maxStart (OneX) spécifie le nombre maximal de messages EAPOL-Start envoyés. Une fois que le nombre maximal de messages de EAPOL-Start a été envoyé, le client suppose qu’il n’y a aucun authentificateur présent sur le réseau.

Cet élément est facultatif. Quand maxStart n’est pas spécifié dans un profil, une valeur de 3 messages est utilisée.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.

``` syntax
<xs:element name="maxStart">
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

L’élément **Maxstart** est défini par l’élément [**Onex**](onexschema-onex-element.md) .

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

 

 




