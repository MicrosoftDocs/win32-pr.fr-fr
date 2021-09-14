---
description: La fonction SetCCInstPtr capture un pointeur d’instance de contexte.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: SetCCInstPtr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229596"
---
# <a name="setccinstptr-function"></a>SetCCInstPtr fonction)

La fonction **SetCCInstPtr** capture un pointeur d’instance de contexte.

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpCurCaptureInst* 
</dt> <dd>

Pointeur vers les données d’instance ajoutées à la capture.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Aucun.

## <a name="remarks"></a>Notes

Utilisez cette fonction pour stocker un pointeur vers un bloc qui a été alloué avec la fonction **CCHeapAlloc** . Chaque analyseur peut définir une seule instance de données sur une capture.

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

[GetCCInstPtr](getccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




