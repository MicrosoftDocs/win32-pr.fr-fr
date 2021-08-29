---
description: La fonction CCHeapReAlloc réalloue la mémoire allouée par la fonction CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: CCHeapReAlloc, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0679b80531c679beaee9eaf56be24ae16f6abea566b74d1928d4fa31fbf37747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144332"
---
# <a name="ccheaprealloc-function"></a>CCHeapReAlloc fonction)

La fonction **CCHeapReAlloc** réalloue la mémoire allouée par la fonction **CCHeapAlloc** .

## <a name="syntax"></a>Syntaxe


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpMem* 
</dt> <dd>

Pointeur vers la mémoire allouée d’origine.

</dd> <dt>

*dwBytes* 
</dt> <dd>

Taille de la mémoire réallouée, mesurée en octets.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indique si la mémoire réallouée a été initialisée. Si la valeur du paramètre est **true**, la mémoire nouvellement allouée est initialisée à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire réallouée.

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

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




