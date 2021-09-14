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
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224956"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) sur le convertisseur vidéo.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




