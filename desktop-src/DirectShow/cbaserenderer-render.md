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
ms.openlocfilehash: 185baf6818d2022dbe7b64cfab888945e1a2405433eefa925d2de70dcca286e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016857"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                              |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode virtuelle pure [**CBaseRenderer ::D orendersample**](cbaserenderer-dorendersample.md), qui fait le vrai travail. La classe dérivée doit implémenter **DoRenderSample**.

Juste avant d’appeler **DoRenderSample**, cette méthode appelle la méthode [**CBaseRenderer :: OnRenderStart**](cbaserenderer-onrenderstart.md) . Immédiatement après, il appelle la méthode [**CBaseRenderer :: OnRenderEnd**](cbaserenderer-onrenderend.md) . La classe dérivée peut substituer ces deux méthodes en fonction des besoins.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




