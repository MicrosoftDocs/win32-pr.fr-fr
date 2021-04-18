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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526322"
---
# <a name="crenderedinputpinendofstream-method"></a><span data-ttu-id="1f326-104">Méthode CRenderedInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="1f326-104">CRenderedInputPin.EndOfStream method</span></span>

<span data-ttu-id="1f326-105">La `EndOfStream` méthode indique au code confidentiel qu’aucune donnée supplémentaire n’est attendue, jusqu’à ce qu’une nouvelle commande Run soit envoyée au filtre.</span><span class="sxs-lookup"><span data-stu-id="1f326-105">The `EndOfStream` method notifies the pin that no additional data is expected, until a new run command is issued to the filter.</span></span> <span data-ttu-id="1f326-106">Cette méthode implémente la méthode [**IPIN :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="1f326-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f326-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f326-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="1f326-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f326-108">Parameters</span></span>

<span data-ttu-id="1f326-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1f326-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f326-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f326-110">Return value</span></span>

<span data-ttu-id="1f326-111">Retourne S \_ OK en cas de réussite, ou un code d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1f326-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f326-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1f326-112">Remarks</span></span>

<span data-ttu-id="1f326-113">Si le filtre est en cours d’exécution, cette méthode envoie un événement [**EC \_ complet**](ec-complete.md) au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1f326-113">If the filter is running, this method sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="1f326-114">Dans le cas contraire, définit un indicateur de manière à ce que l’événement ce soit \_ envoyé lors de la prochaine exécution du filtre.</span><span class="sxs-lookup"><span data-stu-id="1f326-114">Otherwise, is sets a flag so that the EC\_COMPLETE event is sent when the filter next runs.</span></span> <span data-ttu-id="1f326-115">Le vidage du filtre efface l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="1f326-115">Flushing the filter clears the flag.</span></span>

<span data-ttu-id="1f326-116">Vous devez remplacer cette méthode pour conserver le verrou de streaming du pin :</span><span class="sxs-lookup"><span data-stu-id="1f326-116">You should override this method to hold the pin's streaming lock:</span></span>


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



<span data-ttu-id="1f326-117">En outre, si le filtre traite les appels de **réception** de manière asynchrone, le code confidentiel doit attendre pour envoyer l' \_ événement EC complet jusqu’à ce que le filtre ait traité tous les échantillons en attente.</span><span class="sxs-lookup"><span data-stu-id="1f326-117">Also, if the filter processes **Receive** calls asynchronously, the pin should wait to send the EC\_COMPLETE event until the filter has processed all pending samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f326-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f326-118">Requirements</span></span>



| <span data-ttu-id="1f326-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f326-119">Requirement</span></span> | <span data-ttu-id="1f326-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f326-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f326-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f326-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1f326-122"><dt>Amextra. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f326-122"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f326-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f326-123">Library</span></span><br/> | <dl> <span data-ttu-id="1f326-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1f326-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f326-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f326-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f326-126">**CRenderedInputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="1f326-126">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




