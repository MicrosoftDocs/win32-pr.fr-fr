---
description: Évalue une expression dans les builds de débogage et de vente au détail. Dans les versions Debug, affiche un message de diagnostic si l’expression a la valeur FALSe.
ms.assetid: 259a3d30-0b20-4430-8b74-83ec619576ae
title: Macro EXECUTE_ASSERT (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXECUTE_ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 871a8e4a04ec1dc31f3240b539a943c9c1733f083166fa4b7e6f6b52d14a466c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401790"
---
# <a name="execute_assert-macro"></a>EXÉCUTER la \_ macro Assert

Évalue une expression dans les builds de débogage et de vente au détail. Dans les versions Debug, affiche un message de diagnostic si l’expression a la **valeur false**.

## <a name="syntax"></a>Syntaxe


```C++
void EXECUTE_ASSERT(
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

## <a name="remarks"></a>Remarques

Contrairement à la macro [**Assert**](assert.md) , cette macro évalue l’expression dans les builds de vente au détail. Dans les versions Debug, si l’expression est **false**, la macro affiche une boîte de message avec le texte de l’expression, le nom du fichier source et le numéro de ligne. L’utilisateur peut ignorer l’assertion, entrer le débogueur ou quitter l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros Assert et Breakpoint](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




