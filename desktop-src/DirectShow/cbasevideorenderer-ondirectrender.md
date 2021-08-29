---
description: La méthode OnDirectRender collecte les informations de minutage qui contrôlent la synchronisation et le contrôle de qualité.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Méthode CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb66169828d8649011c93f8daece4f0d389e82bef0f9d424cd59f2cdc9ae3cf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052169"
---
# <a name="cbasevideorendererondirectrender-method"></a>Méthode CBaseVideoRenderer. OnDirectRender

La méthode **OnDirectRender** collecte les informations de minutage qui contrôlent la synchronisation et le contrôle de qualité.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Appelez cette méthode à la place de [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) et [**OnRenderEnd**](cbasevideorenderer-onrenderend.md). Cette méthode est utilisée par le convertisseur vidéo DirectDraw.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




