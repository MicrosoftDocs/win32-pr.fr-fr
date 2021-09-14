---
description: Spécifie le mot de passe utilisé pour authentifier un utilisateur.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Élément Password (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118081"
---
# <a name="password-userlogoncred-element"></a>Élément Password (UserLogonCred)

L’élément [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) spécifie le mot de passe utilisé pour authentifier un utilisateur.

L’élément est une chaîne allant jusqu’à 255 caractères.

Cet élément est facultatif.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

L’élément **Password** est défini par l’élément [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

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

 

 




