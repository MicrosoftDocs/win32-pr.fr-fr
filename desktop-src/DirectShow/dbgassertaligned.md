---
description: Teste si un pointeur est aligné sur une limite spécifiée. Si ce n’est pas le cas, cette macro appelle la macro Assert. Ignoré dans les builds de vente au détail.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: DbgAssertAligned macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312421"
---
# <a name="dbgassertaligned-macro"></a>DbgAssertAligned macro)

Teste si un pointeur est aligné sur une limite spécifiée. Si ce n’est pas le cas, cette macro appelle la macro [**Assert**](assert.md) . Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ptr* 
</dt> <dd>

Variable pointeur.

</dd> <dt>

*repère* 
</dt> <dd>

Alignement requis.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette macro ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




