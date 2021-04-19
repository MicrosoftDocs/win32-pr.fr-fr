---
description: La méthode OnReceiveFirstSample est appelée quand le filtre reçoit un exemple en pause.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Méthode CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525656"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Méthode CBaseRenderer. OnReceiveFirstSample

La `OnReceiveFirstSample` méthode est appelée lorsque le filtre reçoit un exemple en pause.

## <a name="syntax"></a>Syntaxe


```C++
virtual void OnReceiveFirstSample(
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

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer. Cette méthode est principalement destinée aux convertisseurs vidéo. Lorsqu’un convertisseur vidéo est suspendu, il affiche généralement le premier échantillon sous la forme d’une image continue.

Si vous recherchez le graphique en pause, cette méthode est également appelée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




