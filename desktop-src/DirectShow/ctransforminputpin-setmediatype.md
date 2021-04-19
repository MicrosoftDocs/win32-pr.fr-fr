---
description: La méthode SetMediaType définit le type de média pour la connexion.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Méthode CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531131"
---
# <a name="ctransforminputpinsetmediatype-method"></a>Méthode CTransformInputPin. SetMediaType

La `SetMediaType` méthode définit le type de média pour la connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MT* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui spécifie le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) . Elle appelle la méthode [**CTransformFilter :: SetMediaType**](ctransformfilter-setmediatype.md) du filtre pour informer le filtre.

Le code confidentiel doit vérifier que le type de média est acceptable avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




