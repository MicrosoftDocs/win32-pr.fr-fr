---
description: La fonction GetFrameRecognizeData retourne une table de structures RECOGNIZEDATA. Chacune de ces structures contient un identificateur de protocole et un décalage qui pointe vers le début du protocole spécifié dans les données.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: GetFrameRecognizeData, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2b04472e0fee0238677a6592cace0d1c7fbe078635ac85b92ff8922c68da3c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366497"
---
# <a name="getframerecognizedata-function"></a>GetFrameRecognizeData fonction)

La fonction **GetFrameRecognizeData** retourne une table de structures **RECOGNIZEDATA** . Chacune de ces structures contient un identificateur de protocole et un décalage qui pointe vers le début du protocole spécifié dans les données.

## <a name="syntax"></a>Syntaxe


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers un frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers une structure **RECOGNIZEDATATABLE** .

Si la fonction échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameRecognizeData** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




