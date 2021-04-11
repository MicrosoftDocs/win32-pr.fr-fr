---
description: La fonction GetFrameSrcAddressOffset retourne le décalage de l’adresse source des frames.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: GetFrameSrcAddressOffset, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204011"
---
# <a name="getframesrcaddressoffset-function"></a>GetFrameSrcAddressOffset fonction)

La fonction **GetFrameSrcAddressOffset** retourne le décalage de l’adresse source du frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle vers le frame.

</dd> <dt>

*Typedadresse* 
</dt> <dd>

Type d’adresse source. La valeur du paramètre peut être l’une des suivantes :

-   TYPE d’adresse \_ \_ Ethernet
-   ADRESSE \_ IP du type d’adresse \_
-   TYPE d’adresse \_ \_ IPX
-   TYPE d’adresse \_ \_ TOKENRING
-   TYPE d’adresse \_ \_ FDDI
-   TYPE d’adresse \_ \_ XNS
-   TYPE d’adresse \_ \_ IP Vines \_
-   TYPE d’adresse \_ \_ ATM

</dd> <dt>

*AddressLength* 
</dt> <dd>

Pointeur vers une **valeur DWORD**, qui, en retour, contient la longueur de l’adresse, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est le décalage de l’adresse source.

Si la fonction échoue, la valeur de retour est moins un (-1).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




