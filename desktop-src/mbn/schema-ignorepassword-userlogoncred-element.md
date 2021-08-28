---
description: Indique comment gérer les mots de passe lors de la mise à niveau des profils.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Élément IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 683fafb763e3f8613afa1b8dca99020856d67a03fdb44e993adf032ce166ceab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975168"
---
# <a name="ignorepassword-userlogoncred-element"></a>Élément IgnorePassword (UserLogonCred)

L’élément **IgnorePassword (UserLogonCred)** indique comment gérer les mots de passe lors de la mise à niveau des profils.

Si la valeur est **true** et qu’un profil portant le même nom existe au moment de l’opération de mise à jour, le mot de passe de ce profil est pris et stocké dans le nouveau profil.

Cet élément est facultatif.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

L’élément **IgnorePassword** est défini par l’élément [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Configuration requise



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

 

 




