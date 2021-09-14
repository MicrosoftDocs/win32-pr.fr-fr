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
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222729"
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

## <a name="return-value"></a>Valeur de retour

Si les adresses sont identiques, la fonction retourne la valeur zéro.

Si le paramètre *lpAddress1* spécifie une adresse qui est inférieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre négatif.

Si le paramètre *lpAddress1* spécifie une adresse qui est supérieure à l’adresse que le paramètre *lpAddress2* spécifie, la valeur de retour est un nombre positif.

## <a name="remarks"></a>Notes

Une adresse qui est inférieure à une autre adresse indique un frame précédent. Une adresse supérieure à une autre adresse indique une trame ultérieure.

Moniteur réseau fournit deux autres fonctions, [CompareFrameDestAddress](compareframedestaddress.md) et [CompareFrameSourceAddress](compareframesourceaddress.md), que vous pouvez utiliser pour comparer des adresses. La fonction **CompareFrameDestAddress** compare une adresse donnée à l’adresse de destination du frame, et la fonction **CompareFrameSourceAddress** compare une adresse donnée à l’adresse source du frame.

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

[CompareFrameDestAddress](compareframedestaddress.md)
</dt> <dt>

[CompareFrameSourceAddress](compareframesourceaddress.md)
</dt> </dl>

 

 




