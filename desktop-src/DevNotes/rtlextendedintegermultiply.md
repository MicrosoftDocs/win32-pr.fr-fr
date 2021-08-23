---
description: Multiplie les entiers étendus.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571469"
---
# <a name="rtlextendedintegermultiply-function"></a>RtlExtendedIntegerMultiply fonction)

\[La fonction **RtlExtendedIntegerMultiply** est exportée pour prendre en charge les binaires de pilote existants et est obsolète. Pour de meilleures performances, utilisez la prise en charge du compilateur pour les opérations d’entiers 64 bits.\]

Multiplie les entiers étendus.

## <a name="syntax"></a>Syntaxe


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Multiplicande* \[ dans\]
</dt> <dd>

Multiplicande.

</dd> <dt>

*Multiplicateur* \[ dans\]
</dt> <dd>

Multiplicateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le résultat de la multiplication.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
