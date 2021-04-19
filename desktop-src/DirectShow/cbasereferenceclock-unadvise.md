---
description: 'La méthode Unadvise supprime une demande de notification en attente. Cette méthode implémente la méthode IReferenceClock :: Unadvise.'
ms.assetid: b137234a-e260-42f9-b583-9e6a5fd7bca4
title: CBaseReferenceClock. Unadvise, méthode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14daf1d34c8a6a923ec7e181ac69f9ecbae0160a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543911"
---
# <a name="cbasereferenceclockunadvise-method"></a><span data-ttu-id="adc29-104">CBaseReferenceClock. Unadvise, méthode</span><span class="sxs-lookup"><span data-stu-id="adc29-104">CBaseReferenceClock.Unadvise method</span></span>

<span data-ttu-id="adc29-105">La `Unadvise` méthode supprime une demande de notification en attente.</span><span class="sxs-lookup"><span data-stu-id="adc29-105">The `Unadvise` method removes a pending advise request.</span></span> <span data-ttu-id="adc29-106">Cette méthode implémente la méthode [**IReferenceClock :: Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) .</span><span class="sxs-lookup"><span data-stu-id="adc29-106">This method implements the [**IReferenceClock::Unadvise**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-unadvise) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adc29-107">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="adc29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adc29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc29-109">*dwAdviseToken*</span><span class="sxs-lookup"><span data-stu-id="adc29-109">*dwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="adc29-110">Identificateur de la demande à supprimer.</span><span class="sxs-lookup"><span data-stu-id="adc29-110">Identifier of the request to remove.</span></span> <span data-ttu-id="adc29-111">Utilisez la valeur retournée par les méthodes [**CBaseReferenceClock :: AdviseTime**](cbasereferenceclock-advisetime.md) ou [**CBaseReferenceClock :: AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) dans le paramètre *pdwAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="adc29-111">Use the value returned by the [**CBaseReferenceClock::AdviseTime**](cbasereferenceclock-advisetime.md) or [**CBaseReferenceClock::AdvisePeriodic**](cbasereferenceclock-adviseperiodic.md) methods in the *pdwAdviseToken* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc29-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="adc29-112">Return value</span></span>

<span data-ttu-id="adc29-113">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="adc29-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="adc29-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="adc29-114">Return code</span></span>                                                                             | <span data-ttu-id="adc29-115">Description</span><span class="sxs-lookup"><span data-stu-id="adc29-115">Description</span></span>           |
|-----------------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="adc29-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="adc29-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="adc29-117">Introuvable.</span><span class="sxs-lookup"><span data-stu-id="adc29-117">Not found.</span></span><br/> |
| <dl> <span data-ttu-id="adc29-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="adc29-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="adc29-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="adc29-119">Success.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="adc29-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adc29-120">Requirements</span></span>



| <span data-ttu-id="adc29-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adc29-121">Requirement</span></span> | <span data-ttu-id="adc29-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="adc29-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adc29-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="adc29-123">Header</span></span><br/>  | <dl> <span data-ttu-id="adc29-124"><dt>Refclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adc29-124"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="adc29-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="adc29-125">Library</span></span><br/> | <dl> <span data-ttu-id="adc29-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="adc29-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc29-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adc29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc29-128">**CBaseReferenceClock, classe**</span><span class="sxs-lookup"><span data-stu-id="adc29-128">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




