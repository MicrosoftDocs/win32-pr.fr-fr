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
ms.openlocfilehash: caf429437d284a27e4cda830b51e4512375310f2d466a597e58c394a2fea551f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501629"
---
# <a name="validatereadptr-macro"></a>ValidateReadPtr macro)

Vérifie que le processus appelant dispose d’un accès en lecture à un bloc de mémoire. Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Cette macro est déconseillée. dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.

 

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

## <a name="remarks"></a>Remarques

cette macro est ignorée sauf si debug, \_ debug ou VFWROBUST est défini lorsque le DirectShow fichier d’en-tête de classe de base est inclus. Cette macro peut avoir un impact significatif sur les performances.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros de validation du pointeur](pointer-validation-macros.md)
</dt> </dl>

 

 




