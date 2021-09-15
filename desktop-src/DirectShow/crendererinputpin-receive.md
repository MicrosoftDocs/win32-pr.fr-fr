---
description: 'La méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode remplace la méthode CBaseInputPin :: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: CRendererInputPin. Receive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312445"
---
# <a name="crendererinputpinreceive-method"></a>CRendererInputPin. Receive, méthode

La `Receive` méthode reçoit l’échantillon de média suivant dans le flux. Cette méthode remplace la méthode [**CBaseInputPin :: Receive**](cbaseinputpin-receive.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) du filtre, qui gère le rendu. Si cette méthode échoue, le code PIN envoie un \_ événement EC ERRORABORT.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRendererInputPin, classe**](crendererinputpin.md)
</dt> </dl>

 

 




