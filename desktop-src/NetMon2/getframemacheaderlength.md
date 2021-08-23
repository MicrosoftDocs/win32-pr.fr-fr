---
description: La fonction GetFrameMacHeaderLength retourne la longueur, en octets, de l’en-tête MAC du frame.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: GetFrameMacHeaderLength, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0e6c4abe859cd4c307d8ade586b9371b69b5c171681006cf4aa1634ef815d794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743899"
---
# <a name="getframemacheaderlength-function"></a>GetFrameMacHeaderLength fonction)

La fonction **GetFrameMacHeaderLength** retourne la longueur, en octets, de l’en-tête Mac du frame.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est la longueur en octets de l’en-tête MAC.

Si la fonction échoue, ou si un type MAC inconnu est rencontré, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetFrameMacHeaderLength** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




