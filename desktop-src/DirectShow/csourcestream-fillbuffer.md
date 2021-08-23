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
ms.openlocfilehash: b9a522dd2b10e7ced60b65c84621bb1817be4b8abbca8656ba23f49e95fe3892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687399"
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



 

## <a name="remarks"></a>Remarques

La classe dérivée doit implémenter cette méthode.

L’exemple de support fourni à cette méthode n’a pas de datage. La classe dérivée doit appeler la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) pour définir les horodatages. Si cela est approprié pour le type de média, la classe dérivée doit également définir les heures de média, en appelant la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) . Pour plus d’informations, consultez [temps et horloges dans DirectShow](time-and-clocks-in-directshow.md).

Retourne S \_ false à la fin du flux. Cela amène la classe **CSourceStream** à envoyer la notification de fin de flux et à arrêter la boucle de traitement de la mémoire tampon. Pour plus d’informations, consultez [**CSourceStream ::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Source. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSourceStream, classe**](csourcestream.md)
</dt> </dl>

 

 




