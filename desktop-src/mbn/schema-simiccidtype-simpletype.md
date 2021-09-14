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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220921"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




