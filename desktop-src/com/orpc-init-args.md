---
title: Structure ORPC_INIT_ARGS
description: La \_ \_ structure d’arguments ORPC init contient des informations utilisées pour initialiser le débogage à distance à l’aide de l’interface IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- Structure COM ORPC_INIT_ARGS
- Pointeur de structure LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103256"
---
# <a name="orpc_init_args-structure"></a>ORPC \_ Init, \_ structure d’arguments

La structure d' **\_ \_ arguments ORPC init** contient des informations utilisées pour initialiser le débogage à distance à l’aide de l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Membres

<dl> <dt>

**lpIntfOrpcDebug**
</dt> <dd>

Pointeur vers l’interface [**IOrpcDebugNotify**](iorpcdebugnotify.md) pour une utilisation par les débogueurs in-process. Si le débogueur n’est pas in-process ou s’il s’agit d’un système Macintosh, ce champ doit avoir la **valeur null**.

</dd> <dt>

**pvPSN**
</dt> <dd>

Pointeur vers le numéro de série du processus Macintosh du processus du programme débogué. Si le programme débogué n’est pas un système Macintosh, ce champ doit avoir la **valeur null**.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Réservé. Doit être égal à 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Réservé. Doit être égal à 0.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORPC \_ dbg \_ tout**](orpc-dbg-all.md)
</dt> <dt>

[**\_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





