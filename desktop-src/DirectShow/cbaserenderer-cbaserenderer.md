---
description: Méthode constructeur CBaseRenderer. CBaseRenderer.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Constructeur CBaseRenderer. CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119907"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="18576-103">Constructeur CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="18576-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="18576-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="18576-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="18576-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18576-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="18576-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18576-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="18576-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="18576-108">Identificateur de classe du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="18576-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="18576-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="18576-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="18576-110">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="18576-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="18576-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="18576-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="18576-112">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="18576-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="18576-113">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="18576-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="18576-114">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="18576-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18576-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="18576-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="18576-116">Reçoit une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18576-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="18576-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="18576-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="18576-118">Résolution de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="18576-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18576-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18576-119">Requirements</span></span>



| <span data-ttu-id="18576-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18576-120">Requirement</span></span> | <span data-ttu-id="18576-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="18576-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18576-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="18576-122">Header</span></span><br/>  | <dl> <span data-ttu-id="18576-123"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18576-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="18576-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18576-124">Library</span></span><br/> | <dl> <span data-ttu-id="18576-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="18576-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18576-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18576-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18576-127">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="18576-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




