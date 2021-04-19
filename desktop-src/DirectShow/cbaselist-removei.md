---
description: La méthode Removei supprime l’élément à la position spécifiée.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: CBaseList. Removei, méthode (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537591"
---
# <a name="cbaselistremovei-method"></a>CBaseList. Removei, méthode

La `RemoveI` méthode supprime l’élément à la position spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* 
</dt> <dd>

Valeur de POSITION indiquant l’élément à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’élément.

## <a name="remarks"></a>Notes

Cette méthode supprime le nœud de la liste, mais ne supprime pas l’élément contenu dans ce nœud.

Si *pos* a la **valeur null**, la méthode retourne la **valeur null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxlist. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseList, classe**](cbaselist.md)
</dt> </dl>

 

 




