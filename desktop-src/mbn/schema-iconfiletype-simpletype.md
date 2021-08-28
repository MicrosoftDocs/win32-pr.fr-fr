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
ms.openlocfilehash: a4ad0c27c40c1b647a15a2c53ed67ffc1deee590006e7e9a514c11f6285c6bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975248"
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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




