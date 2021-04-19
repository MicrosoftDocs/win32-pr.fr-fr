---
description: 'La méthode GetPreroll récupère le temps de préroll. Cette méthode implémente la méthode IMediaSeeking :: GetPreroll.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Méthode CSourceSeeking. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543818"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="fad49-104">Méthode CSourceSeeking. GetPreroll</span><span class="sxs-lookup"><span data-stu-id="fad49-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="fad49-105">La `GetPreroll` méthode récupère le temps de préroll.</span><span class="sxs-lookup"><span data-stu-id="fad49-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="fad49-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="fad49-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fad49-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="fad49-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fad49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad49-109">*pPreroll*</span><span class="sxs-lookup"><span data-stu-id="fad49-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="fad49-110">Pointeur vers une variable qui reçoit le temps de préroll.</span><span class="sxs-lookup"><span data-stu-id="fad49-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="fad49-111">La valeur est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="fad49-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad49-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fad49-112">Return value</span></span>

<span data-ttu-id="fad49-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fad49-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fad49-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fad49-114">Return code</span></span>                                                                               | <span data-ttu-id="fad49-115">Description</span><span class="sxs-lookup"><span data-stu-id="fad49-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fad49-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fad49-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fad49-117">Succès</span><span class="sxs-lookup"><span data-stu-id="fad49-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="fad49-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="fad49-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fad49-119">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="fad49-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fad49-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fad49-120">Requirements</span></span>



| <span data-ttu-id="fad49-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fad49-121">Requirement</span></span> | <span data-ttu-id="fad49-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad49-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fad49-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="fad49-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fad49-124"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fad49-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fad49-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fad49-125">Library</span></span><br/> | <dl> <span data-ttu-id="fad49-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fad49-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad49-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad49-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad49-128">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="fad49-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




