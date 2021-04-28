---
description: Méthode constructeur CAMThread. CAMThread.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructeur CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096407"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="460b1-103">Constructeur CAMThread. CAMThread</span><span class="sxs-lookup"><span data-stu-id="460b1-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="460b1-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="460b1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="460b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="460b1-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="460b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="460b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460b1-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="460b1-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="460b1-108">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="460b1-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="460b1-109">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="460b1-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="460b1-110">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="460b1-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="460b1-111">Pour la compatibilité descendante avec les versions antérieures de strmbase. lib, la valeur par défaut de ce paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="460b1-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="460b1-112">Toutefois, le passage d’une valeur non **null** est préférable, afin que l’appelant puisse vérifier l’état de l’objet.</span><span class="sxs-lookup"><span data-stu-id="460b1-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="460b1-113">Notes </span><span class="sxs-lookup"><span data-stu-id="460b1-113">Remarks</span></span>

<span data-ttu-id="460b1-114">La méthode de constructeur ne crée pas le thread.</span><span class="sxs-lookup"><span data-stu-id="460b1-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="460b1-115">Pour créer le thread, appelez la méthode [**CAMThread :: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="460b1-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="460b1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="460b1-116">Requirements</span></span>



| <span data-ttu-id="460b1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="460b1-117">Requirement</span></span> | <span data-ttu-id="460b1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="460b1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460b1-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="460b1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="460b1-120"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="460b1-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="460b1-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="460b1-121">Library</span></span><br/> | <dl> <span data-ttu-id="460b1-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="460b1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="460b1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="460b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460b1-124">**CAMThread, classe**</span><span class="sxs-lookup"><span data-stu-id="460b1-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




