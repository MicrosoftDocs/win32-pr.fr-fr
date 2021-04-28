---
description: 'Méthode CSourceSeeking. GetRate : la méthode GetRate récupère la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: GetRate.'
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
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085227"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="d39be-104">Méthode CSourceSeeking. GetRate</span><span class="sxs-lookup"><span data-stu-id="d39be-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="d39be-105">La `GetRate` méthode récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="d39be-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="d39be-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="d39be-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d39be-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="d39be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d39be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d39be-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="d39be-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d39be-110">Pointeur vers une variable qui reçoit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="d39be-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d39be-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d39be-111">Return value</span></span>

<span data-ttu-id="d39be-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d39be-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d39be-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d39be-113">Return code</span></span>                                                                               | <span data-ttu-id="d39be-114">Description</span><span class="sxs-lookup"><span data-stu-id="d39be-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d39be-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d39be-116">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="d39be-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d39be-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d39be-118">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="d39be-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d39be-119">Notes </span><span class="sxs-lookup"><span data-stu-id="d39be-119">Remarks</span></span>

<span data-ttu-id="d39be-120">La vitesse de lecture est spécifiée par la variable membre [**CSourceSeeking :: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="d39be-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d39be-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d39be-121">Requirements</span></span>



| <span data-ttu-id="d39be-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d39be-122">Requirement</span></span> | <span data-ttu-id="d39be-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d39be-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d39be-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="d39be-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d39be-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d39be-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d39be-126">Library</span></span><br/> | <dl> <span data-ttu-id="d39be-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d39be-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d39be-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d39be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39be-129">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="d39be-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




