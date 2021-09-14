---
description: La méthode Receive reçoit l’exemple de support suivant dans le flux.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: CBaseRenderer. Receive, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010103"
---
# <a name="cbaserendererreceive-method"></a>CBaseRenderer. Receive, méthode

La `Receive` méthode reçoit l’échantillon de média suivant dans le flux.

## <a name="syntax"></a>Syntaxe


```C++
virtual Receive(
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

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes

La broche d’entrée appelle cette méthode lorsqu’elle reçoit un échantillon du filtre en amont.

Si le filtre est en cours d’exécution, cette méthode effectue les étapes suivantes :

1.  Planifie l’exemple de rendu ([**CBaseRenderer ::P reparereceive**](cbaserenderer-preparereceive.md)).
2.  Attend l’heure planifiée ([**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).
3.  Génère le rendu de l’exemple ([**CBaseRenderer :: Render**](cbaserenderer-render.md)).
4.  Libère l’exemple ([**CBaseRenderer :: ClearPendingSample**](cbaserenderer-clearpendingsample.md)).

Si le filtre est suspendu, la méthode effectue les étapes suivantes :

1.  Notifie la classe dérivée qu’un exemple est disponible ([**CBaseRenderer :: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).
2.  Attend l’heure planifiée.
3.  Génère le rendu de l’exemple.
4.  Libère l’exemple.

Pendant la suspension, la méthode attend à l’étape 2 jusqu’à ce que le filtre bascule vers un état d’exécution. À ce stade, le filtre planifie l’exemple.

Dans la classe de base, la méthode **OnReceiveFirstSample** n’a aucun effet. La classe dérivée peut la substituer. Par exemple, lorsqu’un convertisseur vidéo est suspendu, il affiche le premier échantillon sous la forme d’une image continue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




