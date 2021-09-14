---
description: La macro NOTE envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Remarque (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853678"
---
# <a name="note"></a>REMARQUE

La `NOTE` macro envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*
</dt> <dd>

Chaîne de format printf-style.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*Arg1*–*Arg5*
</dt> <dd>

Arguments supplémentaires pour la chaîne de format. Le nombre d’arguments doit correspondre au nom de la macro. Par exemple, **Note1** accepte un argument et **Note5** accepte cinq arguments.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces macros sont des variantes de la macro [**DbgLog**](dbglog.md) . Ils génèrent des messages de suivi de niveau 5 \_ .

## <a name="example"></a>Exemple


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de sortie de débogage](debug-output-functions.md)
</dt> </dl>

 

 




