---
description: La méthode SetFilterGraph spécifie le récepteur d’événements pour les événements de contrôle de flux.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Méthode CBaseStreamControl. SetFilterGraph (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502639"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Méthode CBaseStreamControl. SetFilterGraph

La `SetFilterGraph` méthode spécifie le récepteur d’événements pour les événements de contrôle de flux.

## <a name="syntax"></a>Syntaxe


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSink* 
</dt> <dd>

pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) du gestionnaire de Graph, ou **NULL** lorsque le filtre quitte le graphique de filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Appelez cette méthode à l’intérieur de la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) du filtre. La classe **CBaseStreamControl** utilise l’interface **IMediaEventSink** pour envoyer le contrôle de flux de [**ce qui \_ \_ \_ a démarré**](ec-stream-control-started.md) et les événements de [**contrôle de flux EC \_ \_ \_ arrêtés**](ec-stream-control-stopped.md) .

Si votre filtre dérive de **CBaseFilter**, appelez d’abord la méthode [**CBaseFilter :: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , qui définit la variable de membre [**CBaseFilter :: m \_ pSink**](cbasefilter-m-psink.md) . Transmettez ensuite **m \_ pSink** à la `SetFilterGraph` méthode. Notez que **m \_ pSink** a la **valeur null** lorsque le filtre quitte le graphique, ce qui est correct.

## <a name="examples"></a>Exemples


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




