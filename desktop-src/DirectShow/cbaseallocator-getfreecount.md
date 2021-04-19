---
description: La méthode GetFreeCount récupère le nombre d’exemples de supports qui ne sont pas utilisés.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Méthode CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543296"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="992d9-103">Méthode CBaseAllocator. GetFreeCount</span><span class="sxs-lookup"><span data-stu-id="992d9-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="992d9-104">La `GetFreeCount` méthode récupère le nombre d’exemples de supports qui ne sont pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="992d9-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="992d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="992d9-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="992d9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="992d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992d9-107">*plBuffersFree*</span><span class="sxs-lookup"><span data-stu-id="992d9-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="992d9-108">Adresse d’une variable qui reçoit le nombre d’exemples qui ne sont pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="992d9-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992d9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="992d9-109">Return value</span></span>

<span data-ttu-id="992d9-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="992d9-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="992d9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="992d9-111">Remarks</span></span>

<span data-ttu-id="992d9-112">Cette méthode implémente la méthode [**IMemAllocatorCallbackTemp :: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) .</span><span class="sxs-lookup"><span data-stu-id="992d9-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="992d9-113">L’Allocator n’expose pas l’interface IMemAllocatorCallbackTemp, sauf si l’indicateur *fEnableReleaseCallback* a la valeur **true** dans le constructeur CBaseAllocator.</span><span class="sxs-lookup"><span data-stu-id="992d9-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="992d9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="992d9-114">Requirements</span></span>



| <span data-ttu-id="992d9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="992d9-115">Requirement</span></span> | <span data-ttu-id="992d9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="992d9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992d9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="992d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="992d9-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="992d9-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="992d9-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="992d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="992d9-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="992d9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992d9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="992d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992d9-122">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="992d9-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




