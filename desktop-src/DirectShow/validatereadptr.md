---
description: Vérifie que le processus appelant dispose d’un accès en lecture à un bloc de mémoire. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 1a70e4e5-e144-4cfe-b6be-c0a70aac9ada
title: ValidateReadPtr macro (Wxdebug. h)
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
ms.openlocfilehash: aa8093ecbd428cafbf1266179b1489cac0d69c4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543956"
---
# <a name="validatereadptr-macro"></a>ValidateReadPtr macro)

Vérifie que le processus appelant dispose d’un accès en lecture à un bloc de mémoire. Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Cette macro est déconseillée. Dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.

 

## <a name="syntax"></a>Syntaxe


```C++
void ValidateReadPtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Pointeur vers un bloc de mémoire.

</dd> <dt>

*libéré* 
</dt> <dd>

Taille du bloc de mémoire, en octets.

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

 

 




