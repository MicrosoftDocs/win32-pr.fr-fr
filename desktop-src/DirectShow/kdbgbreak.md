---
description: Provoque une exception de point d’arrêt et journalise la chaîne spécifiée à l’aide de la macro DbgLog. Ignoré dans les builds de vente au détail.
ms.assetid: 475810db-692b-4727-9ef1-ece74e9618d0
title: KDbgBreak macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KDbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 9631dc8d956652137810b25ae5923cc1c6927bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540994"
---
# <a name="kdbgbreak-macro"></a>KDbgBreak macro)

Provoque une exception de point d’arrêt et journalise la chaîne spécifiée à l’aide de la macro [**DbgLog**](dbglog.md) . Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void KDbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strLiteral* 
</dt> <dd>

Chaîne de texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Contrairement à la macro [**DbgBreak**](dbgbreak.md) , cette macro n’affiche pas de boîte de message invitant l’utilisateur. Dans les versions Debug, il provoque automatiquement une exception de point d’arrêt.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




