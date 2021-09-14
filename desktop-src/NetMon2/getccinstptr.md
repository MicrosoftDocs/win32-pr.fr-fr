---
description: La fonction GetCCInstPtr retourne le pointeur vers les données d’instance ajoutées au contexte de capture.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: GetCCInstPtr, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119278"
---
# <a name="getccinstptr-function"></a>GetCCInstPtr fonction)

La fonction **GetCCInstPtr** retourne le pointeur vers les données d’instance ajoutées au contexte de capture.

## <a name="syntax"></a>Syntaxe


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers les données d’instance d’une capture spécifique.

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

[SetCCInstPtr](setccinstptr.md)
</dt> <dt>

[CCHeapAlloc](ccheapalloc.md)
</dt> <dt>

[CCHeapFree](ccheapfree.md)
</dt> <dt>

[CCHeapReAlloc](ccheaprealloc.md)
</dt> <dt>

[CCHeapSize](ccheapsize.md)
</dt> </dl>

 

 




