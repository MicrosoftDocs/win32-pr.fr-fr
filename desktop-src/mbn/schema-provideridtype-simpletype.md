---
description: Définit un type pour l’élément ProviderID du profil haut débit mobile.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: Type simple providerIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112891"
---
# <a name="provideridtype-simple-type"></a>Type simple providerIdType

Le type simple **providerIdType** définit un type pour l’élément [**ProviderID**](schema-providerid-providertype-element.md) du profil haut débit mobile. Ce type est une collection de chiffres d’au moins un chiffre long et de 6 chiffres au maximum.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **providerIdType** est un jeton qui est limité par le modèle suivant :

-   `\d{1,6}`

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




