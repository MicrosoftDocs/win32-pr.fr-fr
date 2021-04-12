---
description: La fonction GetPropertyText retourne un pointeur vers le texte de la propriété.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: GetPropertyText, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318077"
---
# <a name="getpropertytext-function"></a>GetPropertyText fonction)

La fonction **GetPropertyText** retourne un pointeur vers le texte de la propriété.

## <a name="syntax"></a>Syntaxe


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFrame* \[ dans\]
</dt> <dd>

Handle vers le frame.

</dd> <dt>

*lpPI* \[ dans\]
</dt> <dd>

Pointeur vers une instance de propriété.

</dd> <dt>

*szBuffer* \[ dans\]
</dt> <dd>

Pointeur désignant la chaîne de texte de la propriété.

</dd> <dt>

*BufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de la chaîne de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers le texte de la propriété.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetPropertyText** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




