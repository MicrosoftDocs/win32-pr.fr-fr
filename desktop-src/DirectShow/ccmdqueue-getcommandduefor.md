---
description: La méthode GetCommandDueFor récupère une commande différée planifiée à une heure spécifiée.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Méthode CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530374"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="772c1-103">Méthode CCmdQueue. GetCommandDueFor</span><span class="sxs-lookup"><span data-stu-id="772c1-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="772c1-104">La `GetCommandDueFor` méthode récupère une commande différée qui est planifiée à une heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="772c1-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="772c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="772c1-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="772c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="772c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772c1-107">*tStream*</span><span class="sxs-lookup"><span data-stu-id="772c1-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="772c1-108">Heure pour laquelle la commande est planifiée.</span><span class="sxs-lookup"><span data-stu-id="772c1-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="772c1-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="772c1-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="772c1-110">Adresse d’un pointeur vers la commande différée à exécuter au moment spécifié dans le paramètre *tStream* .</span><span class="sxs-lookup"><span data-stu-id="772c1-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772c1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="772c1-111">Return value</span></span>

<span data-ttu-id="772c1-112">Retourne VFW \_ E \_ \_ introuvable si aucune commande n’est due ; sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="772c1-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="772c1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="772c1-113">Remarks</span></span>

<span data-ttu-id="772c1-114">Cette fonction membre prend un temps de flux et retourne la commande différée planifiée à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="772c1-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="772c1-115">Le décalage de temps de flux réel est calculé lors de l’exécution de la file d’attente de commandes.</span><span class="sxs-lookup"><span data-stu-id="772c1-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="772c1-116">Les commandes restent en file d’attente jusqu’à l’exécution ou l’annulation.</span><span class="sxs-lookup"><span data-stu-id="772c1-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="772c1-117">Cette fonction membre ne sera pas bloquée.</span><span class="sxs-lookup"><span data-stu-id="772c1-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="772c1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="772c1-118">Requirements</span></span>



| <span data-ttu-id="772c1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="772c1-119">Requirement</span></span> | <span data-ttu-id="772c1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="772c1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="772c1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="772c1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="772c1-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="772c1-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="772c1-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="772c1-123">Library</span></span><br/> | <dl> <span data-ttu-id="772c1-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="772c1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="772c1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="772c1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772c1-126">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="772c1-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




