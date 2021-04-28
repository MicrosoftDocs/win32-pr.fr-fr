---
description: 'Méthode CPosPassThru. SetTimeFormat : la méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode IMediaSeeking :: SetTimeFormat.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Méthode CPosPassThru. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085467"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="42384-104">Méthode CPosPassThru. SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="42384-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="42384-105">La méthode SetTimeFormat définit le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="42384-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="42384-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="42384-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42384-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42384-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="42384-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42384-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="42384-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="42384-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="42384-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42384-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="42384-111">Return value</span></span>

<span data-ttu-id="42384-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="42384-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="42384-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42384-113">Requirements</span></span>



| <span data-ttu-id="42384-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42384-114">Requirement</span></span> | <span data-ttu-id="42384-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="42384-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42384-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="42384-116">Header</span></span><br/>  | <dl> <span data-ttu-id="42384-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42384-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42384-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42384-118">Library</span></span><br/> | <dl> <span data-ttu-id="42384-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="42384-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42384-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42384-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42384-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="42384-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="42384-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="42384-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




