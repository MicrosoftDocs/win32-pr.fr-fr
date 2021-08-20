---
description: La fonction DestroyHandoffTable détruit une table de remise créée avec CreateHandoffTable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: DestroyHandoffTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ec956ff4d0098b5a8992d6d28ab10afb925e76cb95b55d85ea7aa813ab2ba3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796265"
---
# <a name="destroyhandofftable-function"></a>DestroyHandoffTable fonction)

La fonction **DestroyHandoffTable** détruit une table de remise créée avec **CreateHandoffTable**.

## <a name="syntax"></a>Syntaxe


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htable* \[ dans\]
</dt> <dd>

Handle vers la table de remise détruite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Aucun.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




