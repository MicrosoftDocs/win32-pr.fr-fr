---
description: La méthode DoBufferProcessingLoop génère des données multimédias et les remet à la broche d’entrée en aval.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Méthode CSourceStream. DoBufferProcessingLoop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d23df592abd125fd64362af89b6f81c5e9dcc20f0aa6cc998974a8fd2d4d87f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953738"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>Méthode CSourceStream. DoBufferProcessingLoop

La `DoBufferProcessingLoop` méthode génère des données multimédias et les remet à la broche d’entrée en aval.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le thread a reçu une demande d’arrêt.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>    | Le flux est terminé, ou le filtre en aval n’accepte pas les exemples.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode implémente la boucle principale qui traite les données et les remet en aval. Chaque fois que vous parcourez la boucle, la méthode récupère un échantillon de média vide à partir de l’allocateur. Il passe l’exemple à la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) . La méthode **FillBuffer** , que la classe dérivée doit implémenter, génère des données multimédias et les place dans l’exemple de mémoire tampon.

La boucle se termine lorsque l’un des éléments suivants se produit :

-   La méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de la broche d’entrée rejette un exemple.
-   La méthode **FillBuffer** retourne S \_ false, indiquant la fin du flux, ou retourne un code d’erreur.
-   Le thread reçoit une demande [**CSourceStream :: Stop**](csourcestream-stop.md) .

La `DoBufferProcessingLoop` méthode gère la notification de fin de flux. Si une erreur se produit, elle envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de graphique de filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




