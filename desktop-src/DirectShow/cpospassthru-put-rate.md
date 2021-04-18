---
description: La méthode de taux de placement \_ définit la vitesse de lecture. Cette méthode implémente la méthode IMediaPosition ::p ut \_ rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Méthode CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525929"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="94227-104">Méthode de taux de CPosPassThru. put \_</span><span class="sxs-lookup"><span data-stu-id="94227-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="94227-105">La `put_Rate` méthode définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="94227-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="94227-106">Cette méthode implémente la méthode [**IMediaPosition ::p ut \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .</span><span class="sxs-lookup"><span data-stu-id="94227-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94227-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94227-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="94227-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94227-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="94227-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="94227-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="94227-110">Playback rate.</span></span> <span data-ttu-id="94227-111">Ne doit pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="94227-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94227-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94227-112">Return value</span></span>

<span data-ttu-id="94227-113">Retourne E \_ INVALIDARG si *dRate* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="94227-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="94227-114">Sinon, retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="94227-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="94227-115">Notes</span><span class="sxs-lookup"><span data-stu-id="94227-115">Remarks</span></span>

<span data-ttu-id="94227-116">Les taux négatifs indiquent une lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="94227-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="94227-117">Tous les supports ne prennent pas en charge la lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="94227-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="94227-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94227-118">Requirements</span></span>



| <span data-ttu-id="94227-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94227-119">Requirement</span></span> | <span data-ttu-id="94227-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="94227-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94227-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="94227-121">Header</span></span><br/>  | <dl> <span data-ttu-id="94227-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94227-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94227-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94227-123">Library</span></span><br/> | <dl> <span data-ttu-id="94227-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="94227-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94227-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94227-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94227-126">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="94227-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




