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
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529648"
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

Pointeur vers l’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) du gestionnaire de graphique de filtre, ou **null** lorsque le filtre quitte le graphique de filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

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
| En-tête<br/>  | <dl> <dt>Strmctl. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




