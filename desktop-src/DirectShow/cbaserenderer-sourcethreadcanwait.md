---
description: La méthode SourceThreadCanWait contient ou libère le thread de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Méthode CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526670"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="338c4-103">Méthode CBaseRenderer. SourceThreadCanWait</span><span class="sxs-lookup"><span data-stu-id="338c4-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="338c4-104">La `SourceThreadCanWait` méthode conserve ou libère le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="338c4-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="338c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="338c4-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="338c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="338c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="338c4-107">*bCanWait*</span><span class="sxs-lookup"><span data-stu-id="338c4-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="338c4-108">Valeur booléenne indiquant s’il faut conserver le thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="338c4-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="338c4-109">Si la **valeur est true**, le thread de streaming est bloqué lorsque le filtre attend pour afficher les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="338c4-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="338c4-110">Si la **valeur est false**, le thread de streaming est libéré.</span><span class="sxs-lookup"><span data-stu-id="338c4-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="338c4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="338c4-111">Return value</span></span>

<span data-ttu-id="338c4-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="338c4-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="338c4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="338c4-113">Remarks</span></span>

<span data-ttu-id="338c4-114">L’appel de la `SourceThreadCanWait` méthode avec la valeur **false** force le filtre à retourner à partir d’un appel [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqué.</span><span class="sxs-lookup"><span data-stu-id="338c4-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="338c4-115">Lorsque le filtre est en cours d’exécution, il bloque les appels de **réception** jusqu’à l’heure de présentation de l’exemple actuel.</span><span class="sxs-lookup"><span data-stu-id="338c4-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="338c4-116">Lorsque le filtre est suspendu, il bloque les appels de **réception** indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="338c4-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="338c4-117">Ce comportement régit le flux de données dans le flux.</span><span class="sxs-lookup"><span data-stu-id="338c4-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="338c4-118">Toutefois, lorsque le filtre est arrêté ou vidé, il ne doit pas être bloqué.</span><span class="sxs-lookup"><span data-stu-id="338c4-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="338c4-119">Le blocage est contrôlé par la méthode [**CBaseRenderer :: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , qui attend deux événements : [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) et [**CBaseRenderer :: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="338c4-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="338c4-120">L’événement **m \_ RenderEvent** est signalé lorsque l’heure de la présentation arrive.</span><span class="sxs-lookup"><span data-stu-id="338c4-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="338c4-121">L’événement **m \_ ThreadSignal** est signalé lorsque `SourceThreadCanWait` est appelé avec la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="338c4-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="338c4-122">L’appel `SourceThreadCanWait` de avec la valeur **true** réinitialise l’événement.</span><span class="sxs-lookup"><span data-stu-id="338c4-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="338c4-123">Les méthodes [**CBaseRenderer :: Stop**](cbaserenderer-stop.md) et [**CBaseRenderer :: BeginFlush**](cbaserenderer-beginflush.md) appellent `SourceThreadCanWait` avec la valeur **false** (en libérant le thread de diffusion en continu).</span><span class="sxs-lookup"><span data-stu-id="338c4-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="338c4-124">Les méthodes [**CBaseRenderer ::P ause**](cbaserenderer-pause.md), [**CBaseRenderer :: Run**](cbaserenderer-run.md)et [**CBaseRenderer :: EndFlush**](cbaserenderer-endflush.md) appellent `SourceThreadCanWait` avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="338c4-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="338c4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="338c4-125">Requirements</span></span>



| <span data-ttu-id="338c4-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="338c4-126">Requirement</span></span> | <span data-ttu-id="338c4-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="338c4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="338c4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="338c4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="338c4-129"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="338c4-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="338c4-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="338c4-130">Library</span></span><br/> | <dl> <span data-ttu-id="338c4-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="338c4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="338c4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="338c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338c4-133">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="338c4-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




