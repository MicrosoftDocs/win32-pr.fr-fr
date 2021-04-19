---
description: La méthode Receive reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.
ms.assetid: 036b209a-3535-4922-b7e9-dbed25b812f5
title: CTransformFilter. Receive, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67924bffc4d4d80b998e686d80d0e50afcd040ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523437"
---
# <a name="ctransformfilterreceive-method"></a>CTransformFilter. Receive, méthode

La `Receive` méthode reçoit un exemple de support, le traite et remet un échantillon de sortie au filtre en aval.

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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                                         |



 

## <a name="remarks"></a>Notes

La broche d’entrée du filtre appelle cette méthode lorsqu’elle reçoit un exemple. Cette méthode appelle la méthode [**CTransformFilter :: InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) , qui prépare un nouvel exemple de sortie. Elle appelle ensuite la méthode [**CTransformFilter :: Transform**](ctransformfilter-transform.md) , que la classe dérivée doit implémenter. La méthode **Transform** traite les données d’entrée et génère des données de sortie.

Si la méthode **Transform** retourne S \_ false, la `Receive` méthode supprime cet exemple. Sur le premier exemple supprimé, le filtre envoie un événement de [**\_ \_ modification de la qualité ce**](ec-quality-change.md) au gestionnaire de graphes de filtre. Dans le cas contraire, si la méthode **Transform** retourne \_ la valeur OK, le filtre remet l’exemple de sortie. Pour ce faire, il appelle la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sur la broche d’entrée en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




