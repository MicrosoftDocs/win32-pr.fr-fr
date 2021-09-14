---
description: La fonction GetCaptureTotalFrames retourne le nombre total de frames dans la capture.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: GetCaptureTotalFrames, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119286"
---
# <a name="getcapturetotalframes-function"></a>GetCaptureTotalFrames fonction)

La fonction **GetCaptureTotalFrames** retourne le nombre total de frames dans la capture.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle de la capture. Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureTotalFrames** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est le nombre total de frames dans la capture.

Si la fonction échoue, la valeur de retour est 0.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureTotalFrames** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




