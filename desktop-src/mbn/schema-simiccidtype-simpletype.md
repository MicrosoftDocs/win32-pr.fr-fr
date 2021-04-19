---
description: Définit un type pour l’élément SimIccID du profil haut débit mobile.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: Type simple simIccIDType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 410145e659a4845c9c96aaeb76d522de3e0c7b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544685"
---
# <a name="simiccidtype-simple-type"></a>Type simple simIccIDType

Le type simple **simIccIDType** définit un type pour l’élément [**SimIccID**](schema-simiccid-mbnprofile-element.md) du profil haut débit mobile. Ce type est une collection de chiffres et/ou de lettres majuscules et minuscules, d’au moins un caractère et d’une longueur maximale de 20 caractères.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **simIccIDType** est un jeton qui est limité par le modèle suivant :

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




