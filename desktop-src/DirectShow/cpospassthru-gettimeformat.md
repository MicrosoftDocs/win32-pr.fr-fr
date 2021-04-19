---
description: 'La méthode GetTimeFormat récupère le format d’heure actuel. Cette méthode implémente la méthode IMediaSeeking :: GetTimeFormat.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Méthode CPosPassThru. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531125"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="4a3d2-104">Méthode CPosPassThru. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="4a3d2-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="4a3d2-105">La `GetTimeFormat` méthode récupère le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="4a3d2-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="4a3d2-106">Cette méthode implémente la méthode [**IMediaSeeking :: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="4a3d2-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a3d2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a3d2-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4a3d2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a3d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a3d2-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="4a3d2-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4a3d2-110">Pointeur vers une variable qui reçoit un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="4a3d2-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a3d2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a3d2-111">Return value</span></span>

<span data-ttu-id="4a3d2-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="4a3d2-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a3d2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a3d2-113">Requirements</span></span>



| <span data-ttu-id="4a3d2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a3d2-114">Requirement</span></span> | <span data-ttu-id="4a3d2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a3d2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3d2-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a3d2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4a3d2-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3d2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a3d2-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a3d2-118">Library</span></span><br/> | <dl> <span data-ttu-id="4a3d2-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4a3d2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a3d2-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a3d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a3d2-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="4a3d2-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="4a3d2-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="4a3d2-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




