---
description: La méthode CancelNotification annule l’événement du minuteur qui planifie le rendu.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Méthode CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be7366e6e22aa7e984fe4b50ea29edfa840d78380373d521c6cd8bfd226e1a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635169"
---
# <a name="cbaserenderercancelnotification-method"></a>Méthode CBaseRenderer. CancelNotification

La `CancelNotification` méthode annule l’événement de minuterie qui planifie le rendu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Aucun événement de minuterie en attente.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                          |



 

## <a name="remarks"></a>Remarques

Le filtre appelle cette méthode lorsque la diffusion en continu s’arrête. La méthode annule tout rendu planifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




