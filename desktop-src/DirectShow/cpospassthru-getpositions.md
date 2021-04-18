---
description: 'La méthode GetPositions récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaSeeking :: GetPositions.'
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Méthode CPosPassThru. GetPositions (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526339"
---
# <a name="cpospassthrugetpositions-method"></a><span data-ttu-id="d385b-104">Méthode CPosPassThru. GetPositions</span><span class="sxs-lookup"><span data-stu-id="d385b-104">CPosPassThru.GetPositions method</span></span>

<span data-ttu-id="d385b-105">La `GetPositions` méthode récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="d385b-105">The `GetPositions` method retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> <span data-ttu-id="d385b-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) .</span><span class="sxs-lookup"><span data-stu-id="d385b-106">This method implements the [**IMediaSeeking::GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d385b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d385b-107">Syntax</span></span>


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d385b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d385b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d385b-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="d385b-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="d385b-110">Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="d385b-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="d385b-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="d385b-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d385b-112">Pointeur vers une variable qui reçoit la position d’arrêt, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="d385b-112">Pointer to a variable that receives the stop position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d385b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d385b-113">Return value</span></span>

<span data-ttu-id="d385b-114">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="d385b-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d385b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d385b-115">Requirements</span></span>



| <span data-ttu-id="d385b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d385b-116">Requirement</span></span> | <span data-ttu-id="d385b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d385b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d385b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d385b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d385b-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d385b-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d385b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d385b-120">Library</span></span><br/> | <dl> <span data-ttu-id="d385b-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d385b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d385b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d385b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d385b-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="d385b-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




