---
description: La fonction GetFrameDstAddressOffset retourne l’offset à l’adresse de destination d’un frame donné.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: GetFrameDstAddressOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119257"
---
# <a name="getframedstaddressoffset-function"></a>GetFrameDstAddressOffset fonction)

La fonction **GetFrameDstAddressOffset** retourne l’offset à l’adresse de destination d’un frame donné.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> <dt>

*AddressType* \[ dans\]
</dt> <dd>

Type de l’adresse de destination. Spécifiez l'une des valeurs suivantes :

type d’adresse Ethernet adresse type adresse \_ \_ \_ \_ IP \_ type adresse IPX type d’adresse TOKENRING type d’adresse \_ \_ \_ \_ \_ FDDI adresse \_ type XNS adresse type de l’adresse \_ \_ \_ \_ IP \_ type \_ ATM.

</dd> <dt>

*AddressLength* \[ dans\]
</dt> <dd>

Longueur de l’adresse de destination, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est le décalage (en octets) du type d’adresse demandé.

Si la fonction échoue, la valeur de retour est moins un (-1).

## <a name="remarks"></a>Notes

Si le paramètre *AddressType* est défini sur le \_ type d’adresse \_ Ethernet, la valeur de retour de la fonction **GetFrameDstAddressOffset** est toujours égale à zéro. Le décalage d’une adresse Ethernet est toujours égal à zéro.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameDstAddressOffset** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




