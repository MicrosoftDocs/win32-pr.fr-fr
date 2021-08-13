---
description: 'La méthode QueryFilterInfo récupère des informations sur le filtre. Cette méthode implémente la méthode IBaseFilter :: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Méthode CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341739"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Méthode CBaseFilter. QueryFilterInfo

La `QueryFilterInfo` méthode récupère des informations sur le filtre. Cette méthode implémente la méthode [**IBaseFilter :: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pInfo* 
</dt> <dd>

Pointeur vers une structure d' [**\_ informations de filtre**](/windows/win32/api/strmif/ns-strmif-filter_info) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le \_ pointeur S ou OK \_ .

## <a name="remarks"></a>Remarques

Cette méthode copie le nom du filtre à partir de la variable de membre [**CBaseFilter :: m \_ pname**](cbasefilter-m-pname.md) dans le membre **achName** de la structure d’informations de filtre \_ . Si **m \_ pname** a la **valeur null**, la méthode définit **achName** sur L' \\ 0 '.

La méthode définit le membre **pGraph** de la structure d’informations de filtre \_ égal à la variable membre [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md) et incrémente le décompte de références. L’appelant doit libérer l’interface.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




