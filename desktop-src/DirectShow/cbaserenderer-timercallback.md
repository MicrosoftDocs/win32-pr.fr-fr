---
description: La méthode TimerCallback est une méthode de rappel pour l’événement de minuterie de fin de flux.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Méthode CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541750"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="af9fe-103">Méthode CBaseRenderer. TimerCallback</span><span class="sxs-lookup"><span data-stu-id="af9fe-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="af9fe-104">La `TimerCallback` méthode est une méthode de rappel pour l’événement de minuterie de fin de flux.</span><span class="sxs-lookup"><span data-stu-id="af9fe-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af9fe-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="af9fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af9fe-106">Parameters</span></span>

<span data-ttu-id="af9fe-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="af9fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af9fe-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af9fe-108">Return value</span></span>

<span data-ttu-id="af9fe-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="af9fe-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af9fe-110">Notes</span><span class="sxs-lookup"><span data-stu-id="af9fe-110">Remarks</span></span>

<span data-ttu-id="af9fe-111">La méthode [**CBaseRenderer :: SendEndOfStream**](cbaserenderer-sendendofstream.md) utilise un événement de minuteur pour planifier \_ des notifications complètes ec.</span><span class="sxs-lookup"><span data-stu-id="af9fe-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="af9fe-112">La méthode **CBaseRenderer :: TimerCallback** est la fonction de rappel pour l’événement du minuteur.</span><span class="sxs-lookup"><span data-stu-id="af9fe-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="af9fe-113">La `TimerCallback` méthode appelle à nouveau **SendEndOfStream** , et **SendEndOfStream** détermine s’il faut envoyer la \_ notification complète ce ou définir une autre minuterie.</span><span class="sxs-lookup"><span data-stu-id="af9fe-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="af9fe-114">La méthode [**CBaseRenderer :: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) annule l’événement du minuteur.</span><span class="sxs-lookup"><span data-stu-id="af9fe-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9fe-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af9fe-115">Requirements</span></span>



| <span data-ttu-id="af9fe-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af9fe-116">Requirement</span></span> | <span data-ttu-id="af9fe-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="af9fe-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9fe-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="af9fe-118">Header</span></span><br/>  | <dl> <span data-ttu-id="af9fe-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af9fe-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af9fe-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af9fe-120">Library</span></span><br/> | <dl> <span data-ttu-id="af9fe-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af9fe-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9fe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af9fe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9fe-123">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="af9fe-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




