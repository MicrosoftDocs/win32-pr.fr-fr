---
description: La fonction GetProtocolInfo retourne un pointeur vers une valeur d’informations de protocole.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: GetProtocolInfo, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950956"
---
# <a name="getprotocolinfo-function"></a>GetProtocolInfo fonction)

La fonction **GetProtocolInfo** retourne un pointeur vers une valeur d’informations de protocole.

## <a name="syntax"></a>Syntaxe


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProtocol* \[ dans\]
</dt> <dd>

Handle d’un protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers la valeur des informations de protocole.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetProtocolInfo** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




