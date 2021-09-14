---
description: La fonction GetFrameTimeStamp retourne l’horodatage d’un frame donné.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: GetFrameTimeStamp, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123533"
---
# <a name="getframetimestamp-function"></a>GetFrameTimeStamp fonction)

La fonction **GetFrameTimeStamp** retourne l’horodatage d’un frame donné.

## <a name="syntax"></a>Syntaxe


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est l’horodatage du frame en microsecondes.

Si la fonction échoue, la valeur de retour est moins un (-1).

## <a name="remarks"></a>Notes

La fonction **GetFrameTimeStamp** retourne un horodatage qui indique le temps écoulé entre le début du processus de capture et l’enregistrement du frame.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameTimeStamp** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




