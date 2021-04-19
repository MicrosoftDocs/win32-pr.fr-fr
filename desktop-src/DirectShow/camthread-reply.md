---
description: La méthode reply répond à une demande.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: CAMThread. Reply, méthode (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532010"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="73528-103">CAMThread. Reply, méthode</span><span class="sxs-lookup"><span data-stu-id="73528-103">CAMThread.Reply method</span></span>

<span data-ttu-id="73528-104">La `Reply` méthode répond à une demande.</span><span class="sxs-lookup"><span data-stu-id="73528-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="73528-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73528-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="73528-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73528-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="73528-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="73528-108">Valeur à retourner dans la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="73528-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73528-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73528-109">Return value</span></span>

<span data-ttu-id="73528-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="73528-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73528-111">Notes</span><span class="sxs-lookup"><span data-stu-id="73528-111">Remarks</span></span>

<span data-ttu-id="73528-112">La méthode CallWorker se bloque jusqu’à ce que cette méthode soit appelée.</span><span class="sxs-lookup"><span data-stu-id="73528-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="73528-113">Le paramètre *DW* fournit la valeur de retour pour CallWorker.</span><span class="sxs-lookup"><span data-stu-id="73528-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="73528-114">Appelez cette méthode dans votre procédure de thread après avoir récupéré une demande, pour libérer le thread demandeur.</span><span class="sxs-lookup"><span data-stu-id="73528-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="73528-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73528-115">Requirements</span></span>



| <span data-ttu-id="73528-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73528-116">Requirement</span></span> | <span data-ttu-id="73528-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="73528-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73528-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="73528-118">Header</span></span><br/>  | <dl> <span data-ttu-id="73528-119"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73528-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="73528-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73528-120">Library</span></span><br/> | <dl> <span data-ttu-id="73528-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="73528-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73528-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73528-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73528-123">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="73528-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




