---
description: 'La méthode GetPositions récupère la position actuelle et la position d’arrêt. Cette méthode implémente la méthode IMediaSeeking :: GetPositions.'
ms.assetid: f577b052-669b-457d-beab-94f574fef08d
title: Méthode CSourceSeeking. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d95013b12d1ee41867ac73920ca1f9b1ca0bdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540530"
---
# <a name="csourceseekinggetpositions-method"></a><span data-ttu-id="e7721-104">Méthode CSourceSeeking. GetPositions</span><span class="sxs-lookup"><span data-stu-id="e7721-104">CSourceSeeking.GetPositions method</span></span>

<span data-ttu-id="e7721-105">La `GetPositions` méthode récupère la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e7721-105">The `GetPositions` method retrieves the current position and the stop position.</span></span> <span data-ttu-id="e7721-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="e7721-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7721-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7721-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="e7721-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7721-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7721-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="e7721-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="e7721-110">Pointeur vers une variable qui reçoit la position de début.</span><span class="sxs-lookup"><span data-stu-id="e7721-110">Pointer to a variable that receives the start position.</span></span>

</dd> <dt>

<span data-ttu-id="e7721-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="e7721-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="e7721-112">Pointeur vers une variable qui reçoit la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="e7721-112">Pointer to a variable that receives the stop position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7721-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7721-113">Return value</span></span>

<span data-ttu-id="e7721-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7721-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7721-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e7721-115">Remarks</span></span>

<span data-ttu-id="e7721-116">Pour le paramètre *pCurrent* , cette méthode retourne la valeur de la variable membre [**CSourceSeeking :: m \_ rtStart**](csourceseeking-m-rtstart.md) , qui représente l’heure de recherche la plus récente, et non la position de diffusion en continu actuelle.</span><span class="sxs-lookup"><span data-stu-id="e7721-116">For the *pCurrent* parameter, this method returns the value of the [**CSourceSeeking::m\_rtStart**](csourceseeking-m-rtstart.md) member variable, which represents the latest seek time, not the current streaming position.</span></span> <span data-ttu-id="e7721-117">Toutefois, lorsqu’une application appelle **IMediaSeeking :: GetPositions** via le gestionnaire de graphique de filtre, les valeurs proviennent généralement d’un filtre de convertisseur, et non d’un filtre source.</span><span class="sxs-lookup"><span data-stu-id="e7721-117">However, when an application calls **IMediaSeeking::GetPositions** through the filter graph manager, the values typically come from a renderer filter, not a source filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7721-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7721-118">Requirements</span></span>



| <span data-ttu-id="e7721-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7721-119">Requirement</span></span> | <span data-ttu-id="e7721-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7721-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7721-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7721-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e7721-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7721-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e7721-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7721-123">Library</span></span><br/> | <dl> <span data-ttu-id="e7721-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e7721-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7721-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7721-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7721-126">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="e7721-126">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




