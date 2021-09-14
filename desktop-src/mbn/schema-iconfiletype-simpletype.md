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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519524"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




