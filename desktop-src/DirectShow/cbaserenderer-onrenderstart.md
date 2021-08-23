---
description: La méthode OnRenderStart est appelée quand le rendu est sur le le début.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Méthode CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626dc1dbcb82aeec94ebe514e686d197cb17bbdd7807ac38057412617182bf55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157652"
---
# <a name="cbaserendereronrenderstart-method"></a>Méthode CBaseRenderer. OnRenderStart

La `OnRenderStart` méthode est appelée lorsque le rendu est sur le le début.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnRenderStart(
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

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer :: Render**](cbaserenderer-render.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer ; par exemple, pour collecter des données de contrôle qualité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




