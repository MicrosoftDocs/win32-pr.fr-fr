---
description: La fonction BERGetInteger décode un entier encodé BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: BERGetInteger, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867026"
---
# <a name="bergetinteger-function"></a>BERGetInteger fonction)

La fonction **BERGetInteger** décode un entier encodé Ber.

## <a name="syntax"></a>Syntaxe


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCurrentPointer* 
</dt> <dd>

Pointeur vers l’entier décodé.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Pointeur vers le pointeur vers la valeur retournée.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Pointeur vers la longueur d’en-tête retournée.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Pointeur vers la longueur des données.

</dd> <dt>

*ppNext* 
</dt> <dd>

Pointeur vers le pointeur vers l’entrée BER suivante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, si un entier encodé BER valide est trouvé et converti), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




