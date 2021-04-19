---
description: La méthode WaitMsg attend que l’événement soit signalé, tout en distribuant les messages envoyés.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Méthode CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542313"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="c2552-103">Méthode CAMMsgEvent. WaitMsg</span><span class="sxs-lookup"><span data-stu-id="c2552-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="c2552-104">La `WaitMsg` méthode attend que l’événement soit signalé, tout en distribuant les messages envoyés.</span><span class="sxs-lookup"><span data-stu-id="c2552-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2552-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2552-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="c2552-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2552-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2552-107">*dwTimeOut*</span><span class="sxs-lookup"><span data-stu-id="c2552-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="c2552-108">Valeur de délai d’attente facultative, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="c2552-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2552-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2552-109">Return value</span></span>

<span data-ttu-id="c2552-110">Retourne la **valeur true** si l’événement est signalé, ou **false** si le délai d’attente a expiré.</span><span class="sxs-lookup"><span data-stu-id="c2552-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2552-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c2552-111">Remarks</span></span>

<span data-ttu-id="c2552-112">Cette méthode appelle la fonction PeekMessage pour traiter les messages.</span><span class="sxs-lookup"><span data-stu-id="c2552-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="c2552-113">Appelez cette méthode à la place de [**CAMEvent :: wait**](camevent-wait.md) si votre thread doit traiter des messages en attendant un événement.</span><span class="sxs-lookup"><span data-stu-id="c2552-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="c2552-114">Si le thread ne traite pas les messages et qu’un autre thread envoie un message, un interblocage peut se produire.</span><span class="sxs-lookup"><span data-stu-id="c2552-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="c2552-115">Par exemple, supposons que vous créez un thread, puis que vous bloquiez jusqu’à ce que le thread initialise.</span><span class="sxs-lookup"><span data-stu-id="c2552-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="c2552-116">Si le thread envoie un message à votre fenêtre en appelant la fonction SendMessage, cela provoque un interblocage.</span><span class="sxs-lookup"><span data-stu-id="c2552-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="c2552-117">Cela est dû au fait que SendMessage ne retourne pas tant que le message n’a pas été traité.</span><span class="sxs-lookup"><span data-stu-id="c2552-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="c2552-118">L’appel de WaitMsg permet à l’appel SendMessage de retourner, ce qui empêche le blocage.</span><span class="sxs-lookup"><span data-stu-id="c2552-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2552-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2552-119">Requirements</span></span>



| <span data-ttu-id="c2552-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2552-120">Requirement</span></span> | <span data-ttu-id="c2552-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2552-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2552-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2552-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c2552-123"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2552-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c2552-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2552-124">Library</span></span><br/> | <dl> <span data-ttu-id="c2552-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2552-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2552-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2552-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2552-127">**CAMMsgEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="c2552-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




