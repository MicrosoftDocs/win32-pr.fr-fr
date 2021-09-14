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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220961"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




