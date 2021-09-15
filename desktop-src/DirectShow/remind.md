---
description: La macro Reminder génère un rappel au moment de la compilation. Cette macro génère une chaîne qui comprend la chaîne de paramètre, le nom du fichier source et le numéro de ligne.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: RAPPELER (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312306"
---
# <a name="remind"></a>AVERTI

La `REMIND` macro génère un rappel au moment de la compilation. Cette macro génère une chaîne qui comprend la chaîne de paramètre, le nom du fichier source et le numéro de ligne.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Chaîne de texte.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette macro est utile pour générer des avertissements au moment de la compilation :


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
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

 

 




