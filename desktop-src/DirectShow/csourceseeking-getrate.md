---
description: 'La méthode GetRate récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Méthode CSourceSeeking. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b14cad0b043193f7ee410455aaa399e3bcb26715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540335"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="e9943-104">Méthode CSourceSeeking. GetRate</span><span class="sxs-lookup"><span data-stu-id="e9943-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="e9943-105">La `GetRate` méthode récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="e9943-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="e9943-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="e9943-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9943-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9943-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="e9943-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9943-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9943-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="e9943-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="e9943-110">Pointeur vers une variable qui reçoit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="e9943-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9943-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9943-111">Return value</span></span>

<span data-ttu-id="e9943-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9943-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="e9943-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e9943-113">Return code</span></span>                                                                               | <span data-ttu-id="e9943-114">Description</span><span class="sxs-lookup"><span data-stu-id="e9943-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="e9943-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9943-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e9943-116">Succès</span><span class="sxs-lookup"><span data-stu-id="e9943-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="e9943-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9943-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e9943-118">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="e9943-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9943-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e9943-119">Remarks</span></span>

<span data-ttu-id="e9943-120">La vitesse de lecture est spécifiée par la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="e9943-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9943-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9943-121">Requirements</span></span>



| <span data-ttu-id="e9943-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9943-122">Requirement</span></span> | <span data-ttu-id="e9943-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9943-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9943-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9943-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e9943-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9943-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9943-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9943-126">Library</span></span><br/> | <dl> <span data-ttu-id="e9943-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9943-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9943-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9943-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9943-129">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="e9943-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




