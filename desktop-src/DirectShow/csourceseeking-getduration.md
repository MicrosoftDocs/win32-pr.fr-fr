---
description: 'Méthode CSourceSeeking. GetDuration : la méthode GetDuration récupère la durée du flux. Cette méthode implémente la méthode IMediaSeeking :: GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Méthode CSourceSeeking. GetDuration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098767"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="63836-104">Méthode CSourceSeeking. GetDuration</span><span class="sxs-lookup"><span data-stu-id="63836-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="63836-105">La `GetDuration` méthode récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="63836-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="63836-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) .</span><span class="sxs-lookup"><span data-stu-id="63836-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63836-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63836-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="63836-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63836-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63836-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="63836-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="63836-110">Pointeur vers une variable qui reçoit la durée, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="63836-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63836-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63836-111">Return value</span></span>

<span data-ttu-id="63836-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="63836-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="63836-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="63836-113">Return code</span></span>                                                                               | <span data-ttu-id="63836-114">Description</span><span class="sxs-lookup"><span data-stu-id="63836-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="63836-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63836-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="63836-116">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="63836-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="63836-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="63836-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="63836-118">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="63836-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63836-119">Notes </span><span class="sxs-lookup"><span data-stu-id="63836-119">Remarks</span></span>

<span data-ttu-id="63836-120">La durée est spécifiée par la variable membre [**CSourceSeeking :: m \_ rtDuration**](csourceseeking-m-rtduration.md) .</span><span class="sxs-lookup"><span data-stu-id="63836-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="63836-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63836-121">Requirements</span></span>



| <span data-ttu-id="63836-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63836-122">Requirement</span></span> | <span data-ttu-id="63836-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="63836-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63836-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="63836-124">Header</span></span><br/>  | <dl> <span data-ttu-id="63836-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63836-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63836-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63836-126">Library</span></span><br/> | <dl> <span data-ttu-id="63836-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63836-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63836-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63836-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63836-129">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="63836-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




