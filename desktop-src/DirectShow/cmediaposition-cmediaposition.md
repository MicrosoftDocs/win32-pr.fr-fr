---
description: En savoir plus sur la méthode de constructeur CMediaPosition. CMediaPosition (Ctlutil. h). Cette méthode utilise les paramètres’pName’et’pUnk'.
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, paramètres pUnk
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106535847"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="d5a08-104">CMediaPosition. CMediaPosition, constructeur (Ctlutil. h)-pName, paramètres pUnk</span><span class="sxs-lookup"><span data-stu-id="d5a08-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="d5a08-105">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d5a08-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a08-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5a08-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="d5a08-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5a08-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a08-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="d5a08-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d5a08-109">Pointeur vers le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="d5a08-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="d5a08-110">Allouez ce paramètre dans la mémoire statique.</span><span class="sxs-lookup"><span data-stu-id="d5a08-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="d5a08-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d5a08-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d5a08-112">Pointeur vers le propriétaire de cet objet, ou **null** si l’objet n’est pas agrégé.</span><span class="sxs-lookup"><span data-stu-id="d5a08-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5a08-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5a08-113">Requirements</span></span>

| <span data-ttu-id="d5a08-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5a08-114">Requirement</span></span> | <span data-ttu-id="d5a08-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5a08-115">Value</span></span> |
|-|-|
| <span data-ttu-id="d5a08-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5a08-116">Header</span></span> | <span data-ttu-id="d5a08-117">Ctlutil. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="d5a08-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="d5a08-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5a08-118">Library</span></span>| <span data-ttu-id="d5a08-119">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="d5a08-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5a08-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a08-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a08-121">**CMediaPosition, classe**</span><span class="sxs-lookup"><span data-stu-id="d5a08-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




