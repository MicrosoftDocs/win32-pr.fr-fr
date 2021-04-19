---
description: Méthode de constructeur.
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
ms.openlocfilehash: b650e23761c3fe5b3f5014666f90c679f088c4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530505"
---
# <a name="cmemallocatorcmemallocator-constructor"></a><span data-ttu-id="6cdc2-103">Constructeur CMemAllocator. CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="6cdc2-103">CMemAllocator.CMemAllocator constructor</span></span>

<span data-ttu-id="6cdc2-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdc2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cdc2-105">Syntax</span></span>


```C++
CMemAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6cdc2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cdc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cdc2-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6cdc2-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdc2-108">Pointeur vers une chaîne contenant le nom de l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-108">Pointer to a string containing the name of the allocator.</span></span>

</dd> <dt>

<span data-ttu-id="6cdc2-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="6cdc2-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdc2-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="6cdc2-111">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6cdc2-112">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6cdc2-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="6cdc2-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdc2-114">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="6cdc2-114">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6cdc2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cdc2-115">Requirements</span></span>



| <span data-ttu-id="6cdc2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cdc2-116">Requirement</span></span> | <span data-ttu-id="6cdc2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cdc2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdc2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cdc2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6cdc2-119"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cdc2-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6cdc2-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cdc2-120">Library</span></span><br/> | <dl> <span data-ttu-id="6cdc2-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cdc2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cdc2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cdc2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cdc2-123">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="6cdc2-123">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




