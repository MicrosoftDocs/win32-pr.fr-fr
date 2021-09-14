---
description: La fonction GetFrameMacType retourne le type MAC du frame.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: GetFrameMacType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123534"
---
# <a name="getframemactype-function"></a>GetFrameMacType fonction)

La fonction **GetFrameMacType** retourne le type Mac du frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameMacType(
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

La fonction retourne le type MAC du frame, qui peut avoir l’une des valeurs suivantes.

-   \_type Mac \_ inconnu
-   MAC \_ type \_ Ethernet
-   \_type Mac \_ TOKENRING
-   \_type Mac \_ FDDI

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameMacType** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




