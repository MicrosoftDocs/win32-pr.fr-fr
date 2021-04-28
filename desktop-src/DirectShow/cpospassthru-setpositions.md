---
description: 'Méthode CPosPassThru. SetPositions : la méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Méthode CPosPassThru. SetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8c61f24ab51ffe7fa161830ef9a0c8bdd167256
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085477"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="c415d-104">Méthode CPosPassThru. SetPositions</span><span class="sxs-lookup"><span data-stu-id="c415d-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="c415d-105">La `SetPositions` méthode définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="c415d-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="c415d-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="c415d-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c415d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c415d-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c415d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c415d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c415d-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="c415d-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="c415d-110">Pointeur vers une variable qui spécifie la position actuelle, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="c415d-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="c415d-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="c415d-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c415d-112">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c415d-112">Bitwise combination of flags.</span></span> <span data-ttu-id="c415d-113">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="c415d-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="c415d-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="c415d-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="c415d-115">Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="c415d-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="c415d-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="c415d-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c415d-117">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c415d-117">Bitwise combination of flags.</span></span> <span data-ttu-id="c415d-118">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="c415d-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c415d-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c415d-119">Return value</span></span>

<span data-ttu-id="c415d-120">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="c415d-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c415d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c415d-121">Requirements</span></span>



| <span data-ttu-id="c415d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c415d-122">Requirement</span></span> | <span data-ttu-id="c415d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c415d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c415d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c415d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c415d-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c415d-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c415d-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c415d-126">Library</span></span><br/> | <dl> <span data-ttu-id="c415d-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c415d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c415d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c415d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c415d-129">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="c415d-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




