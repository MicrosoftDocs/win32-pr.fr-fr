---
description: En savoir plus sur la méthode de constructeur CMediaPosition. CMediaPosition (Ctlutil. h). Cette méthode utilise les paramètres « pName », « pUnk » et « PHR ».
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Constructeur CMediaPosition. CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106523864"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="3e288-104">CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, pUnk, PHR, paramètres</span><span class="sxs-lookup"><span data-stu-id="3e288-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="3e288-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3e288-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e288-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e288-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="3e288-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e288-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e288-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="3e288-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3e288-109">Pointeur vers le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="3e288-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="3e288-110">Allouez ce paramètre dans la mémoire statique.</span><span class="sxs-lookup"><span data-stu-id="3e288-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e288-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3e288-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3e288-112">Pointeur vers le propriétaire de cet objet, ou **null** si l’objet n’est pas agrégé.</span><span class="sxs-lookup"><span data-stu-id="3e288-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="3e288-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="3e288-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3e288-114">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e288-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e288-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e288-115">Requirements</span></span>

| <span data-ttu-id="3e288-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e288-116">Requirement</span></span> | <span data-ttu-id="3e288-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e288-117">Value</span></span> |
|-|-|
| <span data-ttu-id="3e288-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e288-118">Header</span></span> | <span data-ttu-id="3e288-119">Ctlutil. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="3e288-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="3e288-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3e288-120">Library</span></span>| <span data-ttu-id="3e288-121">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="3e288-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3e288-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e288-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e288-123">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="3e288-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




