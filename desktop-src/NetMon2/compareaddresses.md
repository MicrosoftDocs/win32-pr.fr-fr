---
description: La fonction CompareAddresses compare deux adresses, ce qui indique que l’une des adresses est supérieure, inférieure ou égale à l’autre adresse.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: CompareAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323afb66d251d58bf13670fd335da2bd26ad2193ce03d5aa799ddb0f28e875fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744719"
---
# <a name="compareaddresses-function"></a>CompareAddresses fonction)

La fonction **CompareAddresses** compare deux adresses, ce qui indique que l’une des adresses est supérieure, inférieure ou égale à l’autre adresse.

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpAddress1* \[ dans\]
</dt> <dd>

Pointeur vers la première adresse.

</dd> <dt>

*lpAddress2* \[ dans\]
</dt> <dd>

Pointeur vers la deuxième adresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si les adresses sont identiques, la fonction retourne la valeur zéro.

Si le paramètre *lpAddress1* spécifie une adresse qui est inférieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre négatif.

Si le paramètre *lpAddress1* spécifie une adresse qui est supérieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre positif.

## <a name="remarks"></a>Remarques

Une adresse qui est inférieure à une autre adresse indique un frame précédent. Une adresse supérieure à une autre adresse indique une trame ultérieure.

Moniteur réseau fournit deux autres fonctions, [CompareFrameDestAddress](compareframedestaddress.md) et [CompareFrameSourceAddress](compareframesourceaddress.md), que vous pouvez utiliser pour comparer des adresses. La fonction **CompareFrameDestAddress** compare une adresse donnée à l’adresse de destination du frame, et la fonction **CompareFrameSourceAddress** compare une adresse donnée à l’adresse source du frame.

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




