---
description: 'La méthode IsUsingTimeFormat détermine si un format d’heure spécifié est le format en cours d’utilisation. Cette méthode implémente la méthode IMediaSeeking :: IsUsingTimeFormat.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Méthode CPosPassThru. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540084"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="5ea99-104">Méthode CPosPassThru. IsUsingTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5ea99-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="5ea99-105">La `IsUsingTimeFormat` méthode détermine si un format d’heure spécifié est le format en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5ea99-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="5ea99-106">Cette méthode implémente la méthode [**IMediaSeeking :: IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .</span><span class="sxs-lookup"><span data-stu-id="5ea99-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea99-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ea99-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="5ea99-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ea99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea99-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="5ea99-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5ea99-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="5ea99-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea99-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ea99-111">Return value</span></span>

<span data-ttu-id="5ea99-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="5ea99-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea99-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ea99-113">Requirements</span></span>



| <span data-ttu-id="5ea99-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ea99-114">Requirement</span></span> | <span data-ttu-id="5ea99-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ea99-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea99-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ea99-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5ea99-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea99-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5ea99-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ea99-118">Library</span></span><br/> | <dl> <span data-ttu-id="5ea99-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea99-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea99-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ea99-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea99-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="5ea99-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="5ea99-122">**GUID de format d’heure**</span><span class="sxs-lookup"><span data-stu-id="5ea99-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




