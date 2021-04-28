---
description: Méthode constructeur CRendererPosPassThru. CRendererPosPassThru.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Constructeur CRendererPosPassThru. CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59972f12f0f746ef68c267e3fbd0d071d54193c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085407"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="047cb-103">Constructeur CRendererPosPassThru. CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="047cb-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="047cb-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="047cb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="047cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="047cb-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="047cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="047cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="047cb-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="047cb-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="047cb-108">Pointeur vers le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="047cb-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="047cb-109">Allouez ce paramètre dans la mémoire statique.</span><span class="sxs-lookup"><span data-stu-id="047cb-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="047cb-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="047cb-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="047cb-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="047cb-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="047cb-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="047cb-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="047cb-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="047cb-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="047cb-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="047cb-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="047cb-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="047cb-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="047cb-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="047cb-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="047cb-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="047cb-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="047cb-118">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="047cb-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="047cb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="047cb-119">Requirements</span></span>



| <span data-ttu-id="047cb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="047cb-120">Requirement</span></span> | <span data-ttu-id="047cb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="047cb-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="047cb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="047cb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="047cb-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="047cb-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="047cb-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="047cb-124">Library</span></span><br/> | <dl> <span data-ttu-id="047cb-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="047cb-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




