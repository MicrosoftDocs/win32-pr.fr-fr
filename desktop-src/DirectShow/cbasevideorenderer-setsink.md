---
description: La méthode SetSink définit l’objet IQualityControl qui recevra les messages de qualité.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Méthode CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5fef3eb6bd1b959c6c7246e4aeebf5b42a01ddcecd211f3e1d7860102a6381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697899"
---
# <a name="cbasevideorenderersetsink-method"></a>Méthode CBaseVideoRenderer. SetSink

La `SetSink` méthode définit l’objet [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) qui recevra les messages de qualité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*piqc* 
</dt> <dd>

Pointeur vers l’objet [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) auquel les notifications doivent être envoyées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) sur le convertisseur vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




