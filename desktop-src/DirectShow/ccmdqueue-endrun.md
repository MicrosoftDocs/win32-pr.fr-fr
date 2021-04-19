---
description: La méthode EndRun bascule vers le mode arrêté ou suspendu.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Méthode CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532910"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="01382-103">Méthode CCmdQueue. EndRun</span><span class="sxs-lookup"><span data-stu-id="01382-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="01382-104">La `EndRun` méthode bascule en mode arrêté ou suspendu.</span><span class="sxs-lookup"><span data-stu-id="01382-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="01382-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01382-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="01382-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01382-106">Parameters</span></span>

<span data-ttu-id="01382-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="01382-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01382-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01382-108">Return value</span></span>

<span data-ttu-id="01382-109">Retourne une valeur **HRESULT** qui dépend de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="01382-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="01382-110">Notes</span><span class="sxs-lookup"><span data-stu-id="01382-110">Remarks</span></span>

<span data-ttu-id="01382-111">Le mappage de temps entre le temps de flux et l’heure de présentation n’est pas connu après l’appel de cette fonction membre.</span><span class="sxs-lookup"><span data-stu-id="01382-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="01382-112">Appelez la fonction membre [**CCmdQueue :: Run**](ccmdqueue-run.md) pour effectuer ce mappage.</span><span class="sxs-lookup"><span data-stu-id="01382-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="01382-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01382-113">Requirements</span></span>



| <span data-ttu-id="01382-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01382-114">Requirement</span></span> | <span data-ttu-id="01382-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="01382-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01382-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="01382-116">Header</span></span><br/>  | <dl> <span data-ttu-id="01382-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01382-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01382-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01382-118">Library</span></span><br/> | <dl> <span data-ttu-id="01382-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="01382-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01382-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01382-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01382-121">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="01382-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




