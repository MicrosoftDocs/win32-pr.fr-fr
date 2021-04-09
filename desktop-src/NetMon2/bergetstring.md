---
description: La fonction BERGetString décode une chaîne encodée BER.
ms.assetid: 1f72f061-c0ed-4634-9709-e08c2b9468bb
title: BERGetString, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6f8f864b8042ad49502ae53061e157575192e7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864805"
---
# <a name="bergetstring-function"></a>BERGetString fonction)

La fonction **BERGetString** décode une chaîne encodée Ber.

## <a name="syntax"></a>Syntaxe


```C++
BOOL BERGetString(
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

Pointeur vers la chaîne décodée.

</dd> <dt>

*ppValuePointer* 
</dt> <dd>

Pointeur vers le pointeur de la chaîne décodée.

</dd> <dt>

*pHeaderLength* 
</dt> <dd>

Pointeur vers la longueur d’en-tête retournée.

</dd> <dt>

*pDataLength* 
</dt> <dd>

Pointeur vers la longueur de chaîne.

</dd> <dt>

*ppNext* 
</dt> <dd>

Pointeur vers le pointeur de l’entrée BER suivante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, si une chaîne codée BER valide est décodée), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




