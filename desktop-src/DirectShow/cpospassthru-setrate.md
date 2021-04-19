---
description: 'La méthode sechaque définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Méthode CPosPassThru. se, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532877"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="299be-104">CPosPassThru. se, méthode</span><span class="sxs-lookup"><span data-stu-id="299be-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="299be-105">La `SetRate` méthode définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="299be-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="299be-106">Cette méthode implémente la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.</span><span class="sxs-lookup"><span data-stu-id="299be-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="299be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="299be-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="299be-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="299be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="299be-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="299be-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="299be-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="299be-110">Playback rate.</span></span> <span data-ttu-id="299be-111">Ne doit pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="299be-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="299be-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="299be-112">Return value</span></span>

<span data-ttu-id="299be-113">Retourne E \_ INVALIDARG si *dRate* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="299be-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="299be-114">Sinon, retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="299be-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="299be-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="299be-115">Requirements</span></span>



| <span data-ttu-id="299be-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="299be-116">Requirement</span></span> | <span data-ttu-id="299be-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="299be-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="299be-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="299be-118">Header</span></span><br/>  | <dl> <span data-ttu-id="299be-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="299be-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="299be-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="299be-120">Library</span></span><br/> | <dl> <span data-ttu-id="299be-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="299be-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299be-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="299be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299be-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="299be-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




