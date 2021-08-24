---
description: 'La méthode Stop arrête l’objet. Cette méthode implémente la méthode IMediaFilter :: Stop.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: CBaseMediaFilter. Stop, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: effe2df53508cd9c1f6523356eb7296458208c3ee0e61c1dd12c94bd87b6ad31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793229"
---
# <a name="cbasemediafilterstop-method"></a>CBaseMediaFilter. Stop, méthode

La `Stop` méthode arrête l’objet. Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Dans la classe de base, cette méthode affecte à la variable d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) la valeur State \_ Stopped, mais ne fait rien d’autre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




