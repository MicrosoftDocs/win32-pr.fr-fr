---
description: La méthode Wait est bloquée jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: CAMEvent. Wait, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526392"
---
# <a name="cameventwait-method"></a><span data-ttu-id="36449-103">CAMEvent. Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="36449-103">CAMEvent.Wait method</span></span>

<span data-ttu-id="36449-104">La `Wait` méthode se bloque jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise.</span><span class="sxs-lookup"><span data-stu-id="36449-104">The `Wait` method blocks until the event is signaled, or until a time-out occurs.</span></span>

## <a name="syntax"></a><span data-ttu-id="36449-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36449-105">Syntax</span></span>


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="36449-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36449-107">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="36449-107">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="36449-108">Valeur de délai d’attente facultative, exprimée en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="36449-108">Optional time-out value, represented in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36449-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36449-109">Return value</span></span>

<span data-ttu-id="36449-110">Retourne la **valeur true** si l’événement est signalé.</span><span class="sxs-lookup"><span data-stu-id="36449-110">Returns **TRUE** if the event is signaled.</span></span> <span data-ttu-id="36449-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="36449-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="36449-112">Notes</span><span class="sxs-lookup"><span data-stu-id="36449-112">Remarks</span></span>

<span data-ttu-id="36449-113">Pour les événements de réinitialisation automatique, l’événement est réinitialisé à un État non signalé lorsque cette méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="36449-113">For auto-reset events, the event is reset to a nonsignaled state when this method returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="36449-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36449-114">Requirements</span></span>



| <span data-ttu-id="36449-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36449-115">Requirement</span></span> | <span data-ttu-id="36449-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="36449-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36449-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="36449-117">Header</span></span><br/>  | <dl> <span data-ttu-id="36449-118"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36449-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="36449-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="36449-119">Library</span></span><br/> | <dl> <span data-ttu-id="36449-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="36449-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36449-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36449-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36449-122">**CAMEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="36449-122">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




