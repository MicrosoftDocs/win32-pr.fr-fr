---
description: La fonction CCHeapAlloc alloue de la mémoire sur la base d’une capture par capture.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: CCHeapAlloc, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222777"
---
# <a name="ccheapalloc-function"></a>CCHeapAlloc fonction)

La fonction **CCHeapAlloc** alloue de la mémoire sur la base d’une capture par capture.

## <a name="syntax"></a>Syntaxe


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwBytes* 
</dt> <dd>

Longueur demandée de la mémoire allouée.

</dd> <dt>

*bZeroInit* 
</dt> <dd>

Indique si la mémoire allouée a été initialisée. Si la valeur du paramètre est **true**, la mémoire allouée est initialisée à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire allouée. Lorsque vous avez fini d’utiliser la mémoire allouée, libérez de la mémoire en appelant la fonction [**CCHeapFree**](ccheapfree.md) .

Si la fonction échoue, la valeur de retour est **null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SetCCInstPtr**](setccinstptr.md)
</dt> <dt>

[**GetCCInstPtr**](getccinstptr.md)
</dt> <dt>

[**CCHeapFree**](ccheapfree.md)
</dt> <dt>

[**CCHeapReAlloc**](ccheaprealloc.md)
</dt> <dt>

[**CCHeapSize**](ccheapsize.md)
</dt> </dl>

 

 




