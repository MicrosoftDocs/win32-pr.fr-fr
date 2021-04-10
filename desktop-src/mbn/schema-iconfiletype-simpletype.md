---
description: Définit un type de chaîne pour l’élément ICONFilePath dans le profil haut débit mobile.
ms.assetid: 053bc5b8-fab2-4abe-97f8-ed98aea880b1
title: Type simple iconFileType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- iconFileType
api_type:
- Schema
ms.openlocfilehash: 168c2709f8b3049270711e286a35fbbd11e1ffef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112898"
---
# <a name="iconfiletype-simple-type"></a>Type simple iconFileType

Le type simple **iconFileType** définit un type de chaîne pour l’élément [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md) dans le profil haut débit mobile. Cette chaîne comporte au moins un caractère et 1024 caractères au maximum.

``` syntax
<xs:simpleType name="iconFileType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="1024"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




