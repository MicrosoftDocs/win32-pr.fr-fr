---
description: 'Méthode CPosPassThru. ses : la méthode seplaces définit la vitesse de lecture. Cette méthode implémente la méthode IMediaSeeking :: se.'
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
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095217"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="382f0-104">CPosPassThru. se, méthode</span><span class="sxs-lookup"><span data-stu-id="382f0-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="382f0-105">La `SetRate` méthode définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="382f0-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="382f0-106">Cette méthode implémente la méthode [**IMediaSeeking ::**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) se.</span><span class="sxs-lookup"><span data-stu-id="382f0-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="382f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="382f0-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="382f0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="382f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382f0-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="382f0-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="382f0-110">Vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="382f0-110">Playback rate.</span></span> <span data-ttu-id="382f0-111">Ne doit pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="382f0-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="382f0-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="382f0-112">Return value</span></span>

<span data-ttu-id="382f0-113">Retourne E \_ INVALIDARG si *dRate* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="382f0-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="382f0-114">Sinon, retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="382f0-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="382f0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="382f0-115">Requirements</span></span>



| <span data-ttu-id="382f0-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="382f0-116">Requirement</span></span> | <span data-ttu-id="382f0-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="382f0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="382f0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="382f0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="382f0-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="382f0-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="382f0-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="382f0-120">Library</span></span><br/> | <dl> <span data-ttu-id="382f0-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="382f0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="382f0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="382f0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382f0-123">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="382f0-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




