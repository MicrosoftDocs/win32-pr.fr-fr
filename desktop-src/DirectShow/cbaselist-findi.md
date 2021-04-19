---
description: La méthode Findi récupère la première position qui contient l’élément spécifié.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: CBaseList. Findi, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525499"
---
# <a name="cbaselistfindi-method"></a>CBaseList. Findi, méthode

La `FindI` méthode récupère la première position qui contient l’élément spécifié.

## <a name="syntax"></a>Syntaxe


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObj* 
</dt> <dd>

Pointeur désignant l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur de POSITION, ou **null** si l’élément n’est pas dans la liste.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




