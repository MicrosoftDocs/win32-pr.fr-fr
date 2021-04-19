---
description: La fonction GetFrameStoredLength retourne la longueur du frame.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: GetFrameStoredLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521865"
---
# <a name="getframestoredlength-function"></a>GetFrameStoredLength fonction)

La fonction **GetFrameStoredLength** retourne la longueur du frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est la longueur de la trame telle qu’elle est stockée.

Si la fonction échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameStoredLength** .

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

[GetFrameLength](getframelength.md)
</dt> </dl>

 

 




