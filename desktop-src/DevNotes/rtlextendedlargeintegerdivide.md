---
description: Divise des entiers étendus.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531009"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>RtlExtendedLargeIntegerDivide fonction)

\[La fonction **RtlExtendedLargeIntegerDivide** est exportée pour prendre en charge les binaires de pilote existants et est obsolète. Pour de meilleures performances, utilisez la prise en charge du compilateur pour les opérations d’entiers 64 bits.\]

Divise des entiers étendus.

## <a name="syntax"></a>Syntaxe


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Dividende* \[ dans\]
</dt> <dd>

Détaché.

</dd> <dt>

*Diviseur* \[ dans\]
</dt> <dd>

Division.

</dd> <dt>

*Reste* \[ in, out\]
</dt> <dd>

Pointeur vers le reste de la Division.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le résultat de l’opération de division.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
