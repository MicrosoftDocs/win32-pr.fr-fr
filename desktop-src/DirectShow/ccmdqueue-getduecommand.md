---
description: La méthode GetDueCommand récupère un pointeur vers la commande suivante qui est due.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Méthode CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535239"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="d4d6a-103">Méthode CCmdQueue. GetDueCommand</span><span class="sxs-lookup"><span data-stu-id="d4d6a-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="d4d6a-104">La `GetDueCommand` méthode récupère un pointeur vers la commande suivante qui est due.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d6a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4d6a-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="d4d6a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4d6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d6a-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="d4d6a-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d6a-108">Adresse d’un pointeur vers la commande différée.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="d4d6a-109">*msTimeout*</span><span class="sxs-lookup"><span data-stu-id="d4d6a-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d6a-110">Délai d’attente avant l’expiration du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d6a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4d6a-111">Return value</span></span>

<span data-ttu-id="d4d6a-112">Retourne E \_ Abort si un dépassement de délai se produit.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="d4d6a-113">Retourne S \_ OK en cas de réussite ; sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="d4d6a-114">Retourne un objet qui a été incrémenté à l’aide de **IUnknown :: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d6a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d4d6a-115">Remarks</span></span>

<span data-ttu-id="d4d6a-116">Cette fonction membre se bloque jusqu’à ce qu’une commande en attente soit due.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="d4d6a-117">La fonction membre se bloque pendant la durée, en millisecondes, spécifiée dans le paramètre *msTimeout* .</span><span class="sxs-lookup"><span data-stu-id="d4d6a-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="d4d6a-118">Les commandes au moment du flux sont dues uniquement entre les fonctions membres [**CCmdQueue :: Run**](ccmdqueue-run.md) et [**CCmdQueue :: EndRun**](ccmdqueue-endrun.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d6a-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="d4d6a-119">La commande reste en file d’attente jusqu’à l’exécution ou à l’annulation.</span><span class="sxs-lookup"><span data-stu-id="d4d6a-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d6a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4d6a-120">Requirements</span></span>



| <span data-ttu-id="d4d6a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4d6a-121">Requirement</span></span> | <span data-ttu-id="d4d6a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4d6a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d6a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4d6a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d4d6a-124"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4d6a-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4d6a-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4d6a-125">Library</span></span><br/> | <dl> <span data-ttu-id="d4d6a-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4d6a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d6a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d6a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d6a-128">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="d4d6a-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




