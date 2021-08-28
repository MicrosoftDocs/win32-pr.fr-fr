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
ms.openlocfilehash: 3b2019756213c4e27accf89162e5ba8c541fe23689246bf2f1f47186505f3766
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064049"
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

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est le décalage (en octets) du type d’adresse demandé.

Si la fonction échoue, la valeur de retour est moins un (-1).

## <a name="remarks"></a>Remarques

Si le paramètre *AddressType* est défini sur le \_ type d’adresse \_ Ethernet, la valeur de retour de la fonction **GetFrameDstAddressOffset** est toujours égale à zéro. Le décalage d’une adresse Ethernet est toujours égal à zéro.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameDstAddressOffset** .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




