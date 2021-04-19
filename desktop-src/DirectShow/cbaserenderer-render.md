---
description: La méthode Render restitue un exemple.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: CBaseRenderer. Render, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544128"
---
# <a name="cbaserendererrender-method"></a>CBaseRenderer. Render, méthode

La `Render` méthode restitue un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le filtre est arrêté, ou *pMediaSample* a la **valeur null**.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                              |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode virtuelle pure [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md), qui fait le vrai travail. La classe dérivée doit implémenter **DoRenderSample**.

Juste avant d’appeler **DoRenderSample**, cette méthode appelle la méthode [**CBaseRenderer :: OnRenderStart**](cbaserenderer-onrenderstart.md) . Immédiatement après, il appelle la méthode [**CBaseRenderer :: OnRenderEnd**](cbaserenderer-onrenderend.md) . La classe dérivée peut substituer ces deux méthodes en fonction des besoins.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




