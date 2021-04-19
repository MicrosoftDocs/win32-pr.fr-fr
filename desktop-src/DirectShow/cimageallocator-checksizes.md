---
description: La méthode CheckSizes vérifie les propriétés d’allocateur par rapport au type de média actuel.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Méthode CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535287"
---
# <a name="cimageallocatorchecksizes-method"></a><span data-ttu-id="3a2e8-103">Méthode CImageAllocator. CheckSizes</span><span class="sxs-lookup"><span data-stu-id="3a2e8-103">CImageAllocator.CheckSizes method</span></span>

<span data-ttu-id="3a2e8-104">La `CheckSizes` méthode vérifie les propriétés d’allocateur par rapport au type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-104">The `CheckSizes` method checks allocator properties against the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a2e8-105">Syntax</span></span>


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a><span data-ttu-id="3a2e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2e8-107">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="3a2e8-107">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2e8-108">Pointeur désignant une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui décrit les propriétés d’allocateur demandées.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that describes the requested allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2e8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a2e8-109">Return value</span></span>

<span data-ttu-id="3a2e8-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a2e8-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3a2e8-111">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-111">Possible values include the following.</span></span>



| <span data-ttu-id="3a2e8-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3a2e8-112">Return code</span></span>                                                                                           | <span data-ttu-id="3a2e8-113">Description</span><span class="sxs-lookup"><span data-stu-id="3a2e8-113">Description</span></span>                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a2e8-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e8-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3a2e8-115">Les propriétés demandées sont compatibles avec le type de média.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-115">The requested properties are compatible with the media type.</span></span><br/>     |
| <dl> <span data-ttu-id="3a2e8-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e8-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="3a2e8-117">Les propriétés demandées ne sont pas compatibles avec le type de média.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-117">The requested properties are not compatible with the media type.</span></span><br/> |
| <dl> <span data-ttu-id="3a2e8-118"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e8-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3a2e8-119">Le pin propriétaire n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-119">The owning pin is not connected.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="3a2e8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3a2e8-120">Remarks</span></span>

<span data-ttu-id="3a2e8-121">Lorsque la méthode est retournée, si la valeur de retour est \_ OK, le membre **cbBuffer** de la fonction *pRequest* contient la taille réelle de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-121">When the method returns, if the return value is S\_OK, the **cbBuffer** member of *pRequest* contains the actual buffer size.</span></span> <span data-ttu-id="3a2e8-122">Cela peut être plus grand que la taille demandée, mais ne sera jamais plus petit.</span><span class="sxs-lookup"><span data-stu-id="3a2e8-122">This might be larger than the requested size, but will never be smaller.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2e8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a2e8-123">Requirements</span></span>



| <span data-ttu-id="3a2e8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a2e8-124">Requirement</span></span> | <span data-ttu-id="3a2e8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a2e8-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2e8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a2e8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3a2e8-127"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e8-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a2e8-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a2e8-128">Library</span></span><br/> | <dl> <span data-ttu-id="3a2e8-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e8-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2e8-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a2e8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2e8-131">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="3a2e8-131">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




