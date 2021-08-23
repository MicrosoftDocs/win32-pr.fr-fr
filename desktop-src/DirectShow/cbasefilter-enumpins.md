---
description: 'La méthode EnumPins énumère les codes confidentiels sur ce filtre. Cette méthode implémente la méthode IBaseFilter :: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Méthode CBaseFilter. EnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3cd0be44f768898a530eef20d3e4d5d082d230ff809133c0eb62ceb2308b524b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640579"
---
# <a name="cbasefilterenumpins-method"></a>Méthode CBaseFilter. EnumPins

La `EnumPins` méthode énumère les broches sur ce filtre. Cette méthode implémente la méthode [**IBaseFilter :: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Succès<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante<br/>       |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null**<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode crée une instance de la classe de base [**CEnumPins**](cenumpins.md) et retourne un pointeur vers cet objet, de type **IEnumPins**. La classe **CEnumPins** appelle la méthode [**CBaseFilter :: GetPin**](cbasefilter-getpin.md) du filtre pour énumérer les broches sur le filtre.

Si cette méthode est réussie, l’interface **IEnumPins** a un nombre de références en attente. L’appelant doit libérer l’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




