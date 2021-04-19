---
description: Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: ValidateStringPtr macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 19bf0b9e43ecbbbdea0e11284cd1cb4a058e22cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530029"
---
# <a name="validatestringptr-macro"></a>ValidateStringPtr macro)

Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne. Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Cette macro est déconseillée. Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.

 

## <a name="syntax"></a>Syntaxe


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Pointeur vers une chaîne **TCHAR** terminée par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette macro est ignorée sauf si DEBUG, \_ Debug ou VFWROBUST est défini lorsque le fichier d’en-tête de classe de base DirectShow est inclus. Cette macro peut avoir un impact significatif sur les performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros de validation du pointeur](pointer-validation-macros.md)
</dt> </dl>

 

 




