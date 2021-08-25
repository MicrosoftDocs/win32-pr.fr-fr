---
description: La \_ structure d’informations sur le port \_ 1 identifie un port d’imprimante pris en charge.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Structure PORT_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ff6e4c3a43c35118772aede2e329a2e1e761fc0f147b5a3a9ceeef97bbf8fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947809"
---
# <a name="port_info_1-structure"></a>Structure des informations de PORT \_ \_ 1

La structure d' **\_ informations sur le port \_ 1** identifie un port d’imprimante pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie un port imprimante pris en charge (par exemple, « LPT1 : »).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Informations sur \_ le port 1s** (Unicode) et **\_ \_ informations sur le port \_ 1a** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




