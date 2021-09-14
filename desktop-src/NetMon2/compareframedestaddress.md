---
description: La fonction CompareFrameDestAddress compare une adresse à l’adresse de destination d’un frame.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: CompareFrameDestAddress, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222716"
---
# <a name="compareframedestaddress-function"></a>CompareFrameDestAddress fonction)

La fonction **CompareFrameDestAddress** compare une adresse à l’adresse de destination d’un frame.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CompareFrameDestAddress(
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

## <a name="return-value"></a>Valeur de retour

Si les adresses sont identiques, la valeur de retour est **true**.

Si les adresses ne sont pas les mêmes, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Pour que la fonction **CompareFrameDestAddress** retourne correctement, le type d’adresse de destination doit correspondre au type d’adresse spécifié dans le paramètre *lpAddress* .

Moniteur réseau fournit deux autres fonctions, [CompareFrameSourceAddress](compareframesourceaddress.md) et [CompareAddresses](compareaddresses.md), que vous pouvez utiliser pour comparer des adresses. La fonction **CompareFrameSourceAddress** compare une adresse donnée à l’adresse source du frame, et la fonction **CompareAddress** compare deux adresses données.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **CompareFrameDestAddress** .

## <a name="requirements"></a>Spécifications



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

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




