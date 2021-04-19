---
description: La \_ structure d’objet BLOB KEYSVC définit un objet blob de service de clé. Cette structure est utilisée par la fonction RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Structure KEYSVC_BLOB (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532309"
---
# <a name="keysvc_blob-structure"></a>KEYSVC, \_ structure BLOB

La structure d' **\_ objet BLOB KEYSVC** définit un objet blob de service de clé. Cette structure est utilisée par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Membres

<dl> <dt>

**libéré**
</dt> <dd>

Valeur **ULong** qui spécifie la taille, en octets, de **PB**.

</dd> <dt>

**gérés**
</dt> <dd>

Pointeur vers un **octet** qui contient l’objet BLOB, au format [*PKCS \# 12*](../secgloss/p-gly.md) .

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

[**\_chaîne Unicode \_ KEYSVC**](keysvc-unicode-string.md)
</dt> </dl>

 

 
