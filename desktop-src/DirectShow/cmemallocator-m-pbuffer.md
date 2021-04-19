---
description: Pointeur vers le bloc de mémoire qui contient les mémoires tampons.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Membre CMemAllocator :: m_pBuffer (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525667"
---
# <a name="cmemallocatorm_pbuffer-member"></a><span data-ttu-id="5320d-103">CMemAllocator :: m \_ pBuffer, membre</span><span class="sxs-lookup"><span data-stu-id="5320d-103">CMemAllocator::m\_pBuffer member</span></span>

<span data-ttu-id="5320d-104">Pointeur vers le bloc de mémoire qui contient les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="5320d-104">Pointer to the memory block that contains the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="5320d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5320d-105">Syntax</span></span>


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a><span data-ttu-id="5320d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="5320d-106">Remarks</span></span>

<span data-ttu-id="5320d-107">Les exemples de mémoires tampons sont calculés comme des décalages par rapport à ce pointeur.</span><span class="sxs-lookup"><span data-stu-id="5320d-107">Sample buffers are calculated as offsets from this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5320d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5320d-108">Requirements</span></span>



| <span data-ttu-id="5320d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5320d-109">Requirement</span></span> | <span data-ttu-id="5320d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="5320d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5320d-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="5320d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5320d-112"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5320d-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5320d-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5320d-113">Library</span></span><br/> | <dl> <span data-ttu-id="5320d-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5320d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5320d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5320d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5320d-116">**CMemAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="5320d-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




