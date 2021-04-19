---
description: La fonction GetFrameLength retourne la longueur du frame.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: GetFrameLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514785"
---
# <a name="getframelength-function"></a>GetFrameLength fonction)

La fonction **GetFrameLength** retourne la longueur du frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameLength(
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

Si la fonction réussit, la valeur de retour est la longueur du frame en octets.

Si la fonction échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameLength** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




