---
description: La fonction ModifyFrame modifie un frame existant avec les nouvelles données.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: ModifyFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544689"
---
# <a name="modifyframe-function"></a>ModifyFrame fonction)

La fonction **ModifyFrame** modifie un frame existant avec les nouvelles données.

## <a name="syntax"></a>Syntaxe


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle de la capture. Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **ModifyFrame** .

</dd> <dt>

*FrameNumber* \[ dans\]
</dt> <dd>

Numéro d’index de la trame.

</dd> <dt>

*FrameData* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les nouvelles données de frame.

</dd> <dt>

*FrameLength* \[ dans\]
</dt> <dd>

Longueur des nouvelles données, en octets.

</dd> <dt>

*Horodateur* \[ à\]
</dt> <dd>

Horodatage indiquant la date de modification du frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un handle vers un nouveau Frame.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Si l’appel réussit, la fonction **ModifyFrame** détruit le frame d’origine.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **ModifyFrame** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




