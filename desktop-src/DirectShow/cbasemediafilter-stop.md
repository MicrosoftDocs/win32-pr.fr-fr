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
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239249"
---
# <a name="cbasemediafilterstop-method"></a>CBaseMediaFilter. Stop, méthode

La `Stop` méthode arrête l’objet. Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Dans la classe de base, cette méthode affecte à la variable d' [**\_ État CBaseMediaFilter :: m**](cbasemediafilter-m-state.md) la valeur State \_ Stopped, mais ne fait rien d’autre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseMediaFilter, classe**](cbasemediafilter.md)
</dt> </dl>

 

 




