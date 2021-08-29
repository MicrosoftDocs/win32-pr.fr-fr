---
description: La fonction CompareFrameSourceAddress compare une adresse à l’adresse source d’un frame.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: CompareFrameSourceAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8738f1322f30baeb5152f5f453cc8d77c74405889caaf667a3d73413d9cdad96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891099"
---
# <a name="compareframesourceaddress-function"></a>CompareFrameSourceAddress fonction)

La fonction **CompareFrameSourceAddress** compare une adresse à l’adresse source d’un frame.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers un frame.

</dd> <dt>

*lpAddress* \[ dans\]
</dt> <dd>

Pointeur vers une adresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si les adresses sont identiques, la valeur de retour est **true**.

Si les adresses ne sont pas les mêmes, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Pour que la fonction **CompareFrameSourceAddress** aboutisse, le type d’adresse source doit correspondre au type d’adresse spécifié dans le paramètre *lpAddress* .

Moniteur réseau fournit deux autres fonctions pour comparer des adresses : [CompareFrameDestAddress](compareframedestaddress.md) et [CompareAddresses](compareaddresses.md). La fonction **CompareFrameDestAddress** compare une adresse donnée à l’adresse de destination du frame, et la fonction **CompareAddress** compare deux adresses données.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **CompareFrameSourceAddress** .

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

[CompareAddresses](compareaddresses.md)
</dt> <dt>

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> </dl>

 

 




