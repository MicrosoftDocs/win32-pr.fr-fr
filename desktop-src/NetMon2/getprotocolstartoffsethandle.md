---
description: La fonction GetProtocolStartOffsetHandle retourne le décalage de frame d’un protocole donné.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: GetProtocolStartOffsetHandle, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513176"
---
# <a name="getprotocolstartoffsethandle-function"></a>GetProtocolStartOffsetHandle fonction)

La fonction **GetProtocolStartOffsetHandle** retourne le décalage de frame d’un protocole donné.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers un frame.

</dd> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle d’un protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est le décalage de la trame mesurée en octets.

Si la fonction échoue, la valeur de retour est un (1).

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProtocolStartOffsetHandle** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




