---
description: La fonction MacTypeToAddressType convertit un type MAC donné en type d’adresse.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: MacTypeToAddressType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862858"
---
# <a name="mactypetoaddresstype-function"></a>MacTypeToAddressType fonction)

La fonction **MacTypeToAddressType** convertit un type Mac donné en type d’adresse.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MacType* \[ dans\]
</dt> <dd>

Type MAC à convertir. Spécifiez l'une des valeurs suivantes :

type MAC Ethernet Mac type \_ \_ \_ \_ TOKENRING \_ type \_ de Mac FDDI

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est l’un des types d’adresses suivants.

type d’adresse Ethernet adresse type adresse \_ \_ \_ \_ TOKENRING \_ type \_ FDDI

Si la fonction échoue, le type MAC est inconnu, la valeur de retour est-1.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **MacTypeToAddressType** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




