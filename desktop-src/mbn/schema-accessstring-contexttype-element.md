---
description: Identifie l’APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Élément AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118114"
---
# <a name="accessstring-contexttype-element"></a>Élément AccessString (contextType)

L’élément **AccessString (ContextType)** identifie le APN ou la chaîne de numérotation à utiliser pour établir une connexion de données.

Cet élément peut avoir une longueur maximale de 100 caractères.

Cet élément est facultatif.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément **AccessString** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**Contexte (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




