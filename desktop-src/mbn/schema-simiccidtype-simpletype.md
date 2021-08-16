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
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035757"
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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




