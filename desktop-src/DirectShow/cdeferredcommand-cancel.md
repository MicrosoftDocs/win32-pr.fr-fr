---
description: 'La méthode Cancel annule une demande CDeferredCommand :: Invoke précédemment mise en file d’attente.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: CDeferredCommand. Cancel, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540687"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="09b39-103">CDeferredCommand. Cancel, méthode</span><span class="sxs-lookup"><span data-stu-id="09b39-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="09b39-104">La `Cancel` méthode annule une demande [**CDeferredCommand :: Invoke**](cdeferredcommand-invoke.md) précédemment mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="09b39-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09b39-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="09b39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09b39-106">Parameters</span></span>

<span data-ttu-id="09b39-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="09b39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09b39-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09b39-108">Return value</span></span>

<span data-ttu-id="09b39-109">Retourne VFW \_ E \_ déjà \_ annulé si **m \_ pQueue** a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="09b39-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="09b39-110">Retourne un **HRESULT** à partir de [**CCmdQueue :: Remove**](ccmdqueue-remove.md) si l’appel génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="09b39-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="09b39-111">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="09b39-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="09b39-112">Notes</span><span class="sxs-lookup"><span data-stu-id="09b39-112">Remarks</span></span>

<span data-ttu-id="09b39-113">Cette fonction membre implémente la méthode [**IDeferredCommand :: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .</span><span class="sxs-lookup"><span data-stu-id="09b39-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b39-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09b39-114">Requirements</span></span>



| <span data-ttu-id="09b39-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09b39-115">Requirement</span></span> | <span data-ttu-id="09b39-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b39-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b39-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="09b39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="09b39-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09b39-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09b39-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09b39-119">Library</span></span><br/> | <dl> <span data-ttu-id="09b39-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="09b39-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09b39-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09b39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b39-122">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="09b39-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




