---
description: La \_ \_ structure de chaîne Unicode KEYSVC définit une chaîne Unicode et une longueur maximale pour la chaîne. Cette structure est utilisée par la fonction RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Structure KEYSVC_UNICODE_STRING (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531757"
---
# <a name="keysvc_unicode_string-structure"></a>KEYSVC \_ \_ structure de chaîne Unicode

La structure de **\_ \_ chaîne Unicode KEYSVC** définit une chaîne [*Unicode*](../secgloss/u-gly.md) et une longueur maximale pour la chaîne. Cette structure est utilisée par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Membres

<dl> <dt>

**Durée**
</dt> <dd>

Valeur **UShort** qui spécifie la longueur, en octets, utilisée pour la **mémoire tampon**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Valeur **UShort** qui spécifie la longueur maximale, en octets, autorisée pour la **mémoire tampon**.

</dd> <dt>

**Buffer**
</dt> <dd>

Pointeur vers un **UShort** qui représente la chaîne Unicode.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_objet BLOB KEYSVC**](keysvc-blob.md)
</dt> </dl>

 

 
