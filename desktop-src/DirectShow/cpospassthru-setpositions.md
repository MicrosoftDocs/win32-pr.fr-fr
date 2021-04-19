---
description: 'La méthode SetPositions définit la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: SetPositions.'
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
ms.openlocfilehash: 409b4a63f02e6751f987a53dad2836adecd27607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523455"
---
# <a name="cpospassthrusetpositions-method"></a><span data-ttu-id="4cda8-104">Méthode CPosPassThru. SetPositions</span><span class="sxs-lookup"><span data-stu-id="4cda8-104">CPosPassThru.SetPositions method</span></span>

<span data-ttu-id="4cda8-105">La `SetPositions` méthode définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-105">The `SetPositions` method sets the current position and the stop position.</span></span> <span data-ttu-id="4cda8-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="4cda8-106">This method implements the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cda8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cda8-107">Syntax</span></span>


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4cda8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cda8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cda8-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="4cda8-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="4cda8-110">Pointeur vers une variable qui spécifie la position actuelle, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="4cda8-110">Pointer to a variable that specifies the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="4cda8-111">*dwCurrentFlags*</span><span class="sxs-lookup"><span data-stu-id="4cda8-111">*dwCurrentFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4cda8-112">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4cda8-112">Bitwise combination of flags.</span></span> <span data-ttu-id="4cda8-113">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="4cda8-113">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="4cda8-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="4cda8-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4cda8-115">Pointeur vers une variable qui spécifie l’heure d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="4cda8-115">Pointer to a variable that specifies the stop time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="4cda8-116">*dwStopFlags*</span><span class="sxs-lookup"><span data-stu-id="4cda8-116">*dwStopFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="4cda8-117">Combinaison d’opérations de bits d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="4cda8-117">Bitwise combination of flags.</span></span> <span data-ttu-id="4cda8-118">Pour plus d’informations, consultez [**IMediaSeeking :: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="4cda8-118">See [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cda8-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cda8-119">Return value</span></span>

<span data-ttu-id="4cda8-120">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="4cda8-120">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cda8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cda8-121">Requirements</span></span>



| <span data-ttu-id="4cda8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cda8-122">Requirement</span></span> | <span data-ttu-id="4cda8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cda8-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cda8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cda8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4cda8-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cda8-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cda8-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4cda8-126">Library</span></span><br/> | <dl> <span data-ttu-id="4cda8-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4cda8-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cda8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cda8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cda8-129">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="4cda8-129">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




