---
description: La fonction VarLenSmallIntToDword convertit un petit entier de longueur variable en valeur DWORD.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: VarLenSmallIntToDword, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518430"
---
# <a name="varlensmallinttodword-function"></a>VarLenSmallIntToDword fonction)

La fonction **VarLenSmallIntToDword** convertit un petit entier de longueur variable en valeur **DWORD**.

## <a name="syntax"></a>Syntaxe


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pValue* 
</dt> <dd>

Pointeur vers le petit entier de longueur variable.

</dd> <dt>

*ValueLen* 
</dt> <dd>

Longueur (en octets) de l’entier de longueur variable, petit entier.

</dd> <dt>

*fIsByteswapped* 
</dt> <dd>

Indicateur qui signale si le petit entier de longueur variable est échangé en octets.

</dd> <dt>

*lpDword* 
</dt> <dd>

**DWORD** dans lequel l’entier est converti.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un pointeur vers la valeur **DWORD**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




