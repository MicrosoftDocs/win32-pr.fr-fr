---
description: La méthode FillBuffer remplit un échantillon de média avec des données.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Méthode CSourceStream. FillBuffer (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540244"
---
# <a name="csourcestreamfillbuffer-method"></a>Méthode CSourceStream. FillBuffer

La `FillBuffer` méthode remplit un échantillon de média avec des données.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                             | Description              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Fin de flux<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Succès<br/>       |



 

## <a name="remarks"></a>Notes

La classe dérivée doit implémenter cette méthode.

L’exemple de support fourni à cette méthode n’a pas de datage. La classe dérivée doit appeler la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) pour définir les horodatages. Si cela est approprié pour le type de média, la classe dérivée doit également définir les heures de média, en appelant la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Pour plus d’informations, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).

Retourne S \_ false à la fin du flux. Cela amène la classe **CSourceStream** à envoyer la notification de fin de flux et à arrêter la boucle de traitement de la mémoire tampon. Pour plus d’informations, consultez [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




