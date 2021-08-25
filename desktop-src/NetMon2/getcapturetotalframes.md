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
ms.openlocfilehash: 2a7cae78dd95521fa80dfd9b9637b332c72ed1c82b90ba1f6c932824181ef565
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910779"
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

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est le nombre total de frames dans la capture.

Si la fonction échoue, la valeur de retour est 0.

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureTotalFrames** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




