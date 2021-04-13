---
description: Définit un type de chaîne pour l’élément ProviderName dans le profil haut débit mobile.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: Type simple providerNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526020"
---
# <a name="providernametype-simple-type"></a>Type simple providerNameType

Le type simple **providerNameType** définit un type de chaîne pour l’élément [**providerName**](schema-providername-providertype-element.md) dans le profil haut débit mobile. Cette chaîne doit comporter au moins un caractère et comporter jusqu’à 20 caractères.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




