---
description: Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne ANSI. Si ce n’est pas le cas, la macro appelle la macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: ValidateStringPtrA macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 26a0e000f5b2b8de645924300eb650a05a66a4b57c16c5eda3f124e7bc0903a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432099"
---
# <a name="validatestringptra-macro"></a>ValidateStringPtrA macro)

Vérifie que le processus appelant dispose d’un accès en lecture à une chaîne ANSI. Si ce n’est pas le cas, la macro appelle la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Cette macro est déconseillée. dans le SDK Windows pour Windows Vista (et versions ultérieures), cette macro ne fait rien.

 

## <a name="syntax"></a>Syntaxe


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Pointeur vers une chaîne ANSI terminée par le caractère NULL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

cette macro est ignorée sauf si debug, \_ debug ou VFWROBUST est défini lorsque le DirectShow fichier d’en-tête de classe de base est inclus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros de validation du pointeur](pointer-validation-macros.md)
</dt> </dl>

 

 




