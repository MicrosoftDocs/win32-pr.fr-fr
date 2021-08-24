---
description: 'Méthode CTransformInputPin. SetMediaType : la méthode SetMediaType définit le type de média pour la connexion.'
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
ms.openlocfilehash: 9343f464a7a5abe19c9310ffc7b36e504c02b23abf6b0f88d822815ae9952daf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767569"
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

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: SetMediaType**](cbasepin-setmediatype.md) . Elle appelle la méthode [**CTransformFilter :: SetMediaType**](ctransformfilter-setmediatype.md) du filtre pour informer le filtre.

Le code confidentiel doit vérifier que le type de média est acceptable avant d’appeler cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




