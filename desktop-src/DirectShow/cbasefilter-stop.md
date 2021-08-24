---
description: 'La méthode Stop arrête le filtre. Cette méthode implémente la méthode IMediaFilter :: Stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: CBaseFilter. Stop, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 659ad34c01ca6c74a24f6bbf5f5bef42df46f94f06b7e03541f9caf3398b39e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768189"
---
# <a name="cbasefilterstop-method"></a>CBaseFilter. Stop, méthode

La `Stop` méthode arrête le filtre. Cette méthode implémente la méthode [**IMediaFilter :: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**CBasePin :: inactive**](cbasepin-inactive.md) sur chacune des broches connectées du filtre. Il définit également l’état du filtre sur état \_ arrêté.

Quand le filtre s’arrête, il doit rejeter les exemples en amont, arrêter la diffusion des exemples en aval, arrêter les threads de travail et libérer toutes les ressources qu’il utilisait pour la diffusion en continu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




