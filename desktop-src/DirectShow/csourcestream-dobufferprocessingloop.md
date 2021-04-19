---
description: La méthode DoBufferProcessingLoop génère des données multimédias et les remet à la broche d’entrée en aval.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: Méthode CSourceStream. DoBufferProcessingLoop (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545538"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="09aba-103">Méthode CSourceStream. DoBufferProcessingLoop</span><span class="sxs-lookup"><span data-stu-id="09aba-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="09aba-104">La `DoBufferProcessingLoop` méthode génère des données multimédias et les remet à la broche d’entrée en aval.</span><span class="sxs-lookup"><span data-stu-id="09aba-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="09aba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09aba-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="09aba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09aba-106">Parameters</span></span>

<span data-ttu-id="09aba-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="09aba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09aba-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09aba-108">Return value</span></span>

<span data-ttu-id="09aba-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09aba-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="09aba-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="09aba-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="09aba-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="09aba-111">Return code</span></span>                                                                             | <span data-ttu-id="09aba-112">Description</span><span class="sxs-lookup"><span data-stu-id="09aba-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09aba-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="09aba-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="09aba-114">Le thread a reçu une demande d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="09aba-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="09aba-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09aba-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="09aba-116">Le flux est terminé, ou le filtre en aval n’accepte pas les exemples.</span><span class="sxs-lookup"><span data-stu-id="09aba-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09aba-117">Notes</span><span class="sxs-lookup"><span data-stu-id="09aba-117">Remarks</span></span>

<span data-ttu-id="09aba-118">Cette méthode implémente la boucle principale qui traite les données et les remet en aval.</span><span class="sxs-lookup"><span data-stu-id="09aba-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="09aba-119">Chaque fois que vous parcourez la boucle, la méthode récupère un échantillon de média vide à partir de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="09aba-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="09aba-120">Il passe l’exemple à la méthode [**CSourceStream :: FillBuffer**](csourcestream-fillbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="09aba-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="09aba-121">La méthode **FillBuffer** , que la classe dérivée doit implémenter, génère des données multimédias et les place dans l’exemple de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="09aba-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="09aba-122">La boucle se termine lorsque l’un des éléments suivants se produit :</span><span class="sxs-lookup"><span data-stu-id="09aba-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="09aba-123">La méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) de la broche d’entrée rejette un exemple.</span><span class="sxs-lookup"><span data-stu-id="09aba-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="09aba-124">La méthode **FillBuffer** retourne S \_ false, indiquant la fin du flux, ou retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="09aba-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="09aba-125">Le thread reçoit une demande [**CSourceStream :: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="09aba-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="09aba-126">La `DoBufferProcessingLoop` méthode gère la notification de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="09aba-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="09aba-127">Si une erreur se produit, elle envoie un événement [**EC \_ ERRORABORT**](ec-errorabort.md) au gestionnaire de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="09aba-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="09aba-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09aba-128">Requirements</span></span>



| <span data-ttu-id="09aba-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09aba-129">Requirement</span></span> | <span data-ttu-id="09aba-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="09aba-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09aba-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="09aba-131">Header</span></span><br/>  | <dl> <span data-ttu-id="09aba-132"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09aba-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="09aba-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09aba-133">Library</span></span><br/> | <dl> <span data-ttu-id="09aba-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09aba-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09aba-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09aba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09aba-136">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="09aba-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




