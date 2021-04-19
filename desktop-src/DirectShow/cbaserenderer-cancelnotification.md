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
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532677"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                          |



 

## <a name="remarks"></a>Notes

Le filtre appelle cette méthode lorsque la diffusion en continu s’arrête. La méthode annule tout rendu planifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




