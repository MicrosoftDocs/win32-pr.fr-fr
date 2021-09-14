---
description: Définit un type de chaîne pour le profil haut débit mobile.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: type simple nameType (haut débit mobile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118082"
---
# <a name="nametype-simple-type-mobile-broadband"></a>type simple nameType (haut débit mobile)

Le type simple **NameType** définit un type de chaîne pour le profil haut débit mobile. Cette chaîne comporte au moins un caractère et 255 caractères au maximum.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




