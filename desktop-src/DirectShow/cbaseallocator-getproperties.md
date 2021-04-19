---
description: 'La méthode GetProperties récupère le nombre de mémoires tampons créées par l’allocateur, ainsi que les propriétés de la mémoire tampon. Cette méthode implémente la méthode IMemAllocator :: GetProperties.'
ms.assetid: ccee4d69-52fc-4e3c-b6a4-787914708be4
title: CBaseAllocator. GetProperties, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abf143b11b6dd67fca6c87f9a31ce69f18951311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537983"
---
# <a name="cbaseallocatorgetproperties-method"></a><span data-ttu-id="e24c9-104">CBaseAllocator. GetProperties, méthode</span><span class="sxs-lookup"><span data-stu-id="e24c9-104">CBaseAllocator.GetProperties method</span></span>

<span data-ttu-id="e24c9-105">La `GetProperties` méthode récupère le nombre de mémoires tampons créées par l’allocateur, ainsi que les propriétés de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e24c9-105">The `GetProperties` method retrieves the number of buffers that the allocator will create, and the buffer properties.</span></span> <span data-ttu-id="e24c9-106">Cette méthode implémente la méthode [**IMemAllocator :: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="e24c9-106">This method implements the [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24c9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e24c9-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="e24c9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e24c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24c9-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="e24c9-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="e24c9-110">Pointeur désignant une structure de [**\_ propriétés d’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) qui reçoit les propriétés d’allocateur.</span><span class="sxs-lookup"><span data-stu-id="e24c9-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that receives the allocator properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24c9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e24c9-111">Return value</span></span>

<span data-ttu-id="e24c9-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e24c9-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24c9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e24c9-113">Requirements</span></span>



| <span data-ttu-id="e24c9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e24c9-114">Requirement</span></span> | <span data-ttu-id="e24c9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e24c9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e24c9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e24c9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e24c9-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e24c9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e24c9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e24c9-118">Library</span></span><br/> | <dl> <span data-ttu-id="e24c9-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e24c9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24c9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e24c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24c9-121">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="e24c9-121">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




