---
description: La méthode suivante récupère la position suivante dans la liste.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Méthode CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528749"
---
# <a name="cbaselistnext-method"></a>CBaseList. Next, méthode

La `Next` méthode récupère la position suivante dans la liste.

## <a name="syntax"></a>Syntaxe


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Valeur de POSITION.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur de position qui suit la position spécifiée par *pos*.

## <a name="remarks"></a>Notes

Si *pos* est la dernière position de la liste, la méthode retourne **null**. Si *pos* a la **valeur null**, la méthode retourne la première position dans la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




