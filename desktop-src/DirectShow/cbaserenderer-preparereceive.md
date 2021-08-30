---
description: La méthode PrepareReceive prépare le filtre pour le rendu d’un exemple.
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: Méthode CBaseRenderer. PrepareReceive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c5ff423945de7208de6b876d20d602589e4472671d26f709903b9c34cb7f35c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928639"
---
# <a name="cbaserendererpreparereceive-method"></a>Méthode CBaseRenderer. PrepareReceive

La `PrepareReceive` méthode prépare le filtre pour restituer un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT PrepareReceive(
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

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                             | Description                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                        |
| <dl> <dt>**E \_ échec**</dt> </dl>                  | Échec.<br/>                         |
| <dl> <dt>**E \_ inattendu**</dt> </dl>            | Erreur inattendue.<br/>               |
| <dl> <dt>**exemple de VFW \_ E \_ \_ rejeté**</dt> </dl> | Le filtre supprime cet exemple.<br/> |



 

## <a name="remarks"></a>Remarques

Le filtre appelle cette méthode à l’intérieur de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) , avant d’afficher un exemple. Si le filtre est en cours d’exécution, cette méthode planifie l’exemple de rendu.

Si le filtre a déjà un échantillon en attente, ou si la fin du flux a déjà été atteinte, la méthode retourne E \_ inattendue. Le filtre en amont ne sérialise peut-être pas correctement ses appels de diffusion en continu.

Si l’algorithme de planification détermine que l’exemple doit être supprimé (voir [**CBaseRenderer :: ScheduleSample**](cbaserenderer-schedulesample.md)), la méthode retourne un échantillon de VFW \_ E \_ \_ rejeté. Toutefois, la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de la broche d’entrée ne transmet pas ce code d’erreur au filtre en amont, car la suppression d’un exemple n’est pas une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




