---
description: 'La méthode GetClassID récupère l’identificateur de classe. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Méthode CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520818"
---
# <a name="cbasemediafiltergetclassid-method"></a>Méthode CBaseMediaFilter. GetClassID

La `GetClassID` méthode récupère l’identificateur de classe. Cette méthode implémente la méthode **IPersist :: GetClassID** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClsID* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’identificateur de classe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




