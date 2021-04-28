---
description: Méthode constructeur CMemAllocator. CMemAllocator.
ms.assetid: 2340b39a-cab6-4524-b8cd-b22d4bdd24d0
title: Constructeur CMemAllocator. CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1151572c32efe69cceb89e7a5ea5a045955b5f43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095397"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="ffbc0-103">Constructeur CMemAllocator. CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="ffbc0-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="ffbc0-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffbc0-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ffbc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffbc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffbc0-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ffbc0-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ffbc0-108">Pointeur vers une chaîne contenant le nom de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="ffbc0-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ffbc0-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ffbc0-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="ffbc0-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ffbc0-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ffbc0-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="ffbc0-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ffbc0-114">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ffbc0-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffbc0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffbc0-115">Requirements</span></span>



| <span data-ttu-id="ffbc0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffbc0-116">Requirement</span></span> | <span data-ttu-id="ffbc0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffbc0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbc0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffbc0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ffbc0-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ffbc0-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ffbc0-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ffbc0-120">Library</span></span><br/> | <dl> <span data-ttu-id="ffbc0-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ffbc0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffbc0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffbc0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbc0-123">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="ffbc0-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




