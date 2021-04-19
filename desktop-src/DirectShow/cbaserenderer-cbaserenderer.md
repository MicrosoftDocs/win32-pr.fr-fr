---
description: Méthode de constructeur.
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
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530568"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="ee6c8-103">Constructeur CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="ee6c8-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="ee6c8-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee6c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee6c8-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="ee6c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee6c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee6c8-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="ee6c8-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="ee6c8-108">Identificateur de classe du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="ee6c8-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="ee6c8-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ee6c8-110">Pointeur vers une chaîne contenant le nom du filtre, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="ee6c8-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ee6c8-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ee6c8-112">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="ee6c8-113">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ee6c8-114">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee6c8-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="ee6c8-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ee6c8-116">Reçoit une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee6c8-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="ee6c8-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="ee6c8-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="ee6c8-118">Résolution de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="ee6c8-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee6c8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee6c8-119">Requirements</span></span>



| <span data-ttu-id="ee6c8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee6c8-120">Requirement</span></span> | <span data-ttu-id="ee6c8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee6c8-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee6c8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee6c8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ee6c8-123"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee6c8-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee6c8-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ee6c8-124">Library</span></span><br/> | <dl> <span data-ttu-id="ee6c8-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ee6c8-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee6c8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee6c8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee6c8-127">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="ee6c8-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




