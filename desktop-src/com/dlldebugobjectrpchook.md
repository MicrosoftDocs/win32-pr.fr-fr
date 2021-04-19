---
title: DllDebugObjectRPCHook fonction)
description: Exporté par les DLL COM pour activer le débogage distant.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook fonction COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510360"
---
# <a name="dlldebugobjectrpchook-function"></a>DllDebugObjectRPCHook fonction)

Exporté par les DLL COM pour activer le débogage distant.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fTrace* 
</dt> <dd>

Si la **valeur est true**, le débogage à distance est activé. Si la **valeur est false**, le débogage à distance n’est pas activé.

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ arguments ORPC init**](orpc-init-args.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True** en cas de réussite, **false** dans le cas contraire

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>N/A</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORPC \_ dbg \_ tout**](orpc-dbg-all.md)
</dt> <dt>

[**\_ \_ mémoire tampon dbg ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





