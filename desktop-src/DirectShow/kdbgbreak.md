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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999030"
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

## <a name="return-value"></a>Valeur de retour

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Contrairement à la macro [**DbgBreak**](dbgbreak.md) , cette macro n’affiche pas de boîte de message invitant l’utilisateur. Dans les versions Debug, il provoque automatiquement une exception de point d’arrêt.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




