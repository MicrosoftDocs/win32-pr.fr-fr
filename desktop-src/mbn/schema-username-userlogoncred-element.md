---
description: Spécifie le nom d’utilisateur pour l’ouverture de session.
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: UserName (UserLogonCred), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415859"
---
# <a name="username-userlogoncred-element"></a>UserName (UserLogonCred), élément

L’élément **username (UserLogonCred)** spécifie le nom d’utilisateur pour l’ouverture de session.

L’élément est une chaîne de 255 caractères au maximum.

Cet élément est facultatif.

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

L’élément **username** est défini par l’élément [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**UserLogonCred (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




