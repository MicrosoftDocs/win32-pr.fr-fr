---
description: La macro NAME génère une chaîne de débogage uniquement.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NOM (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107679"
---
# <a name="name"></a>NOM

La macro **Name** génère une chaîne de débogage uniquement.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Chaîne de texte.

</dd> </dl>

## <a name="remarks"></a>Remarques

Dans les versions Debug, cette macro est équivalente à la macro **Text** . Dans les versions commerciales, elle correspond à (TCHAR \* ) **null**. Cette macro est utile lors de la déclaration du nom d’un objet qui dérive de la classe [**CBaseObject**](cbaseobject.md) .


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




