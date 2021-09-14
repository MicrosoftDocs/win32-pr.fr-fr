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
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010114"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                             | Description                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                        |
| <dl> <dt>**E \_ échec**</dt> </dl>                  | Échec.<br/>                         |
| <dl> <dt>**E \_ inattendu**</dt> </dl>            | Erreur inattendue.<br/>               |
| <dl> <dt>**exemple de VFW \_ E \_ \_ rejeté**</dt> </dl> | Le filtre supprime cet exemple.<br/> |



 

## <a name="remarks"></a>Notes

Le filtre appelle cette méthode à l’intérieur de la méthode [**CBaseRenderer :: Receive**](cbaserenderer-receive.md) , avant d’afficher un exemple. Si le filtre est en cours d’exécution, cette méthode planifie l’exemple de rendu.

Si le filtre a déjà un échantillon en attente, ou si la fin du flux a déjà été atteinte, la méthode retourne E \_ inattendue. Le filtre en amont ne sérialise peut-être pas correctement ses appels de diffusion en continu.

Si l’algorithme de planification détermine que l’exemple doit être supprimé (voir [**CBaseRenderer :: ScheduleSample**](cbaserenderer-schedulesample.md)), la méthode retourne un échantillon de VFW \_ E \_ \_ rejeté. Toutefois, la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de la broche d’entrée ne transmet pas ce code d’erreur au filtre en amont, car la suppression d’un exemple n’est pas une erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




