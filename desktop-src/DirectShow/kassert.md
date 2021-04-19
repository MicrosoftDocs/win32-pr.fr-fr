---
description: Évalue une expression et provoque une exception de point d’arrêt si l’expression est FALSe. Le texte de l’expression, le nom du fichier source et le numéro de ligne sont journalisés à l’aide de la macro DbgLog. Ignoré dans les builds de vente au détail.
ms.assetid: fd116403-df23-490f-b3a8-b2a8bf2b4a5f
title: KASSERT macro (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f797e60a6175a86f2c1c9d675e9607a48a58c14a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534907"
---
# <a name="kassert-macro"></a>KASSERT macro)

Évalue une expression et provoque une exception de point d’arrêt si l’expression est **false**. Le texte de l’expression, le nom du fichier source et le numéro de ligne sont journalisés à l’aide de la macro [**DbgLog**](dbglog.md) . Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void KASSERT(
    cond
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*185* 
</dt> <dd>

Expression à évaluer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette macro ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Contrairement aux [](assert.md) macros Assert et [**Execute \_ Assert**](execute-assert.md) , cette macro n’affiche pas de boîte de message invitant l’utilisateur. Dans les versions Debug, si l’expression est **false**, la macro provoque automatiquement l’apparition d’une exception de point d’arrêt.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




