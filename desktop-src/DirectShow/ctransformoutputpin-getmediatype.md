---
description: 'Méthode CTransformOutputPin. GetMediaType : la méthode GetMediaType récupère un type de média préféré, par valeur d’index.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Méthode CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd064934eea6ef2c88a4304466b15811910e8e352041e7242c75650dd54b2a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812779"
---
# <a name="ctransformoutputpingetmediatype-method"></a>Méthode CTransformOutputPin. GetMediaType

La `GetMediaType` méthode récupère un type de média préféré, par valeur d’index.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iPosition* 
</dt> <dd>

Valeur d’index de base zéro.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Pointeur vers un objet [**CMediaType**](cmediatype.md) qui reçoit le type de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                            | Description                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Succès<br/>            |
| <dl> <dt>**VFW \_ S \_ n’a \_ plus d' \_ éléments**</dt> </dl> | Index hors limites<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) . Si la broche d’entrée du filtre n’est pas connectée, la méthode retourne VFW \_ s \_ n’a plus d' \_ \_ éléments. Sinon, elle appelle la méthode [**CTransformFilter :: GetMediaType**](ctransformfilter-getmediatype.md) du filtre pour récupérer le type de média. La méthode **CTransformFilter :: GetMediaType** est virtuelle pure ; la classe dérivée du filtre doit être substituée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




