---
description: La fonction CCHeapSize retourne la taille de la mémoire allouée par la fonction CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: CCHeapSize, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b086777b571af417662bd60a582fbc53a07c49300d21d2c59b6a36d2247b9d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012307"
---
# <a name="ccheapsize-function"></a>CCHeapSize fonction)

La fonction **CCHeapSize** retourne la taille de la mémoire allouée par la fonction **CCHeapAlloc** .

## <a name="syntax"></a>Syntaxe


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpMem* 
</dt> <dd>

Pointeur vers la mémoire allouée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est la taille du bloc de mémoire demandé, mesurée en octets.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> </dl>

 

 




