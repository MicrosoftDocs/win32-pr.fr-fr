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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530414"
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

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IQualityControl :: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) sur le convertisseur vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




