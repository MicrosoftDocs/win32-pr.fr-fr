---
description: La fonction DbgTerminate nettoie la bibliothèque de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: a0e23c57-b4b5-4bcf-8c63-0dee40cc71a7
title: DbgTerminate, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgTerminate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d29e5fde86b9573261e39a0dbe2e9d87018ff23c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224577"
---
# <a name="dbgterminate-function"></a>DbgTerminate fonction)

La fonction **DbgTerminate** nettoie la bibliothèque de débogage. Ignoré dans les builds de vente au détail.

## <a name="syntax"></a>Syntaxe


```C++
void DbgTerminate(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Appelez cette fonction si vous appelez la fonction [**DbgInitialise**](dbginitialise.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




