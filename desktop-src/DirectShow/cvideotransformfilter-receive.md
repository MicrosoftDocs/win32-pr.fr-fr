---
description: 'La méthode Receive reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval. Cette méthode remplace la méthode CTransformFilter :: Receive.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: CVideoTransformFilter. Receive, méthode (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bce69d5f14a522f403eed54b56a340ab02316507766c0cc6d60ff897ec73541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998509"
---
# <a name="cvideotransformfilterreceive-method"></a>CVideoTransformFilter. Receive, méthode

La `Receive` méthode reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval. Cette méthode remplace la méthode [**CTransformFilter :: Receive**](ctransformfilter-receive.md) .

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

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) sur l’exemple d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                             | Description                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Le filtre amont doit cesser d’envoyer des exemples.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                         |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle [**CVideoTransformFilter :: ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) pour déterminer si elle doit remettre cet exemple ou simplement la supprimer. Si **ShouldSkipFrame** retourne **false** (indiquant que l’exemple doit être remis), la méthode effectue les opérations suivantes :

1.  Appelle [**CTransformFilter :: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) pour préparer l’exemple de sortie
2.  Appelle [**CTransformFilter :: Transform**](ctransformfilter-transform.md) pour traiter l’exemple d’entrée. Cette méthode est virtuelle pure et doit être implémentée dans la classe dérivée.
3.  Appelle [**CBaseOutputPin ::D eliver**](cbaseoutputpin-deliver.md) pour fournir l’exemple de sortie.

En outre, cette méthode recherche les modifications de format sur l’exemple d’entrée ou de sortie, en appelant [**IMediaSample :: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype). En cas de modification du format, la méthode définit le type de connexion sur le code confidentiel correspondant. Avant de définir le nouveau type, il appelle **StopStreaming**. Une fois le nouveau type défini, il appelle **StartStreaming**. La classe dérivée peut utiliser ces méthodes pour mettre à jour son état interne. La classe dérivée peut également avoir besoin de vérifier le nouveau format dans sa méthode **Transform** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Vtrans. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CVideoTransformFilter, classe**](cvideotransformfilter.md)
</dt> </dl>

 

 




