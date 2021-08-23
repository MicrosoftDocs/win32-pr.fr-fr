---
description: La fonction GetPreviousProtocolOffsetByName retourne l’instance précédente d’un protocole donné.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: GetPreviousProtocolOffsetByName, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 17b472bbdead74612ccc6d76f1059443ce6f62dd122f7933ae31c99fb82900a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743759"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>GetPreviousProtocolOffsetByName fonction)

La fonction **GetPreviousProtocolOffsetByName** retourne l’instance précédente d’un protocole donné.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> <dt>

*dwStartOffset* \[ dans\]
</dt> <dd>

Décalage dans le frame.

</dd> <dt>

*szProtocolName* \[ dans\]
</dt> <dd>

Nom du protocole que vous souhaitez rechercher.

</dd> <dt>

*pdwPreviousOffset* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui contient l’offset au protocole précédent (si la fonction est réussie).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est le protocole NMERR \_ est \_ \_ introuvable.

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler **GetPreviousProtocolOffsetByName**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




