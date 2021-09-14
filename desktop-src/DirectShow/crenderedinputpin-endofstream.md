---
description: 'La méthode EndOfStream indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue, jusqu’à ce qu’une nouvelle commande Run soit envoyée au filtre. Cette méthode implémente la méthode IPin :: EndOfStream.'
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: Méthode CRenderedInputPin. EndOfStream (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195548"
---
# <a name="crenderedinputpinendofstream-method"></a>Méthode CRenderedInputPin. EndOfStream

La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue, jusqu’à ce qu’une nouvelle commande Run soit envoyée au filtre. Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

si le filtre est en cours d’exécution, cette méthode envoie un événement [**EC \_ complet**](ec-complete.md) à filter Graph Manager. Dans le cas contraire, définit un indicateur de manière à ce que l’événement ce soit \_ envoyé lors de la prochaine exécution du filtre. Le vidage du filtre efface l’indicateur.

Vous devez remplacer cette méthode pour conserver le verrou de streaming du pin :


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



En outre, si le filtre traite les appels de **réception** de manière asynchrone, le code confidentiel doit attendre pour envoyer l' \_ événement EC complet jusqu’à ce que le filtre ait traité tous les échantillons en attente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amextra. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CRenderedInputPin, classe**](crenderedinputpin.md)
</dt> </dl>

 

 




