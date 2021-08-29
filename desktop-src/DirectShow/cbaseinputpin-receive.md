---
description: 'CBaseInputPin. Receive, méthode : la méthode Receive reçoit l’exemple de support suivant dans le flux. Cette méthode implémente la méthode IMemInputPin :: Receive.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: CBaseInputPin. Receive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b9a3ec028b121cfcb76dfe857d4d12b34dca57410ffee177dd45a19e358e29a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341669"
---
# <a name="cbaseinputpinreceive-method"></a>CBaseInputPin. Receive, méthode

La `Receive` méthode reçoit l’échantillon de média suivant dans le flux. Cette méthode implémente la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                             | Description                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                        |
| <dl> <dt>**S \_ false**</dt> </dl>                 | Le code PIN est en cours de vidage ; l’exemple a été rejeté.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                             |
| <dl> <dt>**\_erreur d' \_ exécution VFW E \_**</dt> </dl>   | Une erreur d’exécution s’est produite.<br/>                      |
| <dl> <dt>**VFW \_ E \_ état incorrect \_**</dt> </dl>     | Le code PIN est arrêté.<br/>                             |



 

## <a name="remarks"></a>Remarques

La broche de sortie en amont appelle cette méthode pour remettre un échantillon à la broche d’entrée. La broche d’entrée doit effectuer l’une des opérations suivantes :

-   Traitez l’exemple avant de retourner.
-   Retourner et traiter l’exemple dans un thread de travail.
-   Rejetez l’exemple.

Si le code confidentiel utilise un thread de travail pour traiter l’exemple, ajoutez un décompte de références à l’exemple à l’intérieur de cette méthode. Une fois la méthode retournée, la broche amont libère l’exemple. Lorsque le nombre de références de l’exemple atteint zéro, l’exemple retourne à l’allocateur pour une réutilisation.

Cette méthode est synchrone et peut se bloquer. Si la méthode peut être bloquée, la méthode [**CBaseInputPin :: ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) du pin doit retourner s \_ OK.

Dans la classe de base, cette méthode effectue les étapes suivantes :

1.  Appelle la méthode [**CBaseInputPin :: CheckStreaming**](cbaseinputpin-checkstreaming.md) pour vérifier que le code confidentiel peut traiter des exemples maintenant. Si tel n’est pas le cas, par exemple, si le code PIN est arrêté, la méthode échoue.
2.  Récupère les exemples de propriétés et vérifie si le format a changé (voir ci-dessous).
3.  Si le format a changé, la méthode appelle la méthode [**CBasePin :: CheckMediaType**](cbasepin-checkmediatype.md) pour déterminer si le nouveau format est acceptable.
4.  Si le nouveau format n’est pas acceptable, la méthode appelle la méthode [**CBasePin :: EndOfStream**](cbasepin-endofstream.md) , publie un \_ événement EC ERRORABORT et retourne un code d’erreur.
5.  En supposant qu’il n’y avait pas d’erreur, la méthode retourne S \_ OK.

Testez une modification de format comme suit :

-   Si l’exemple prend en charge l’interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) , vérifiez le membre **dwSampleFlags** de la structure de [**\_ \_ Propriétés am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) . Si l' \_ indicateur AM Sample \_ TYPECHANGED est présent, le format a changé.
-   Sinon, si l’exemple ne prend pas en charge **IMediaSample2**, appelez la méthode [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) . Si la méthode retourne une valeur non **null** , le format a changé.

Dans la classe de base, cette méthode ne traite pas l’exemple. La classe dérivée doit substituer cette méthode pour effectuer le traitement. (Ce que cela implique dépend entièrement du filtre.) La classe dérivée doit appeler la méthode de classe de base pour rechercher les erreurs décrites précédemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseInputPin, classe**](cbaseinputpin.md)
</dt> </dl>

 

 




