---
description: La \_ structure ADDJOB info \_ 1 identifie un travail d’impression ainsi que le répertoire et le fichier dans lequel une application peut stocker ce travail.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Structure ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6a0abcd2d9d09b65e8b4d5dd27e01532859a8060eda7847f0c1b7888a3c9714f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950759"
---
# <a name="addjob_info_1-structure"></a>ADDJOB \_ information \_ 1 (structure)

La structure **ADDJOB \_ info \_ 1** identifie un travail d’impression ainsi que le répertoire et le fichier dans lequel une application peut stocker ce travail.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**Chemin d’accès**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès et le nom de fichier que l’application peut utiliser pour stocker le travail d’impression.

</dd> <dt>

**JobId**
</dt> <dd>

Handle du travail d’impression.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ ADDJOB \_ info \_ 1s** (Unicode) et **\_ ADDJOB \_ info \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




