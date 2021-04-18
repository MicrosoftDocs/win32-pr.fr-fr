---
description: La méthode GetCurrentPosition récupère la position actuelle, par rapport à la durée totale du flux. Non implémenté.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Méthode CSourceSeeking. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52f99323e5ce3a62f1964cad2586a18ad473cdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533352"
---
# <a name="csourceseekinggetcurrentposition-method"></a><span data-ttu-id="0357d-104">Méthode CSourceSeeking. GetCurrentPosition</span><span class="sxs-lookup"><span data-stu-id="0357d-104">CSourceSeeking.GetCurrentPosition method</span></span>

<span data-ttu-id="0357d-105">La `GetCurrentPosition` méthode récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="0357d-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="0357d-106">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="0357d-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="0357d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0357d-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="0357d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0357d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0357d-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="0357d-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="0357d-110">Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="0357d-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0357d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0357d-111">Return value</span></span>

<span data-ttu-id="0357d-112">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="0357d-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0357d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0357d-113">Remarks</span></span>

<span data-ttu-id="0357d-114">En règle générale, les filtres sources ne prennent pas en charge cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0357d-114">Source filters typically do not support this method.</span></span> <span data-ttu-id="0357d-115">Au lieu de cela, les filtres de convertisseur signalent la position actuelle par le biais de la classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0357d-115">Instead, renderer filters report the current position through the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0357d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0357d-116">Requirements</span></span>



| <span data-ttu-id="0357d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0357d-117">Requirement</span></span> | <span data-ttu-id="0357d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0357d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0357d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0357d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0357d-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0357d-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0357d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0357d-121">Library</span></span><br/> | <dl> <span data-ttu-id="0357d-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0357d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0357d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0357d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0357d-124">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="0357d-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




