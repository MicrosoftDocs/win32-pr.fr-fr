---
description: 'La méthode GetTimeFormat récupère le format d’heure actuel. Cette méthode implémente la méthode IMediaSeeking :: GetTimeFormat.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Méthode CSourceSeeking. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540529"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="fcd13-104">Méthode CSourceSeeking. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fcd13-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="fcd13-105">La `GetTimeFormat` méthode récupère le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="fcd13-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="fcd13-106">Cette méthode implémente la méthode [**IMediaSeeking :: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="fcd13-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd13-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcd13-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fcd13-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcd13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd13-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="fcd13-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd13-110">Pointeur vers une variable qui reçoit un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="fcd13-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="fcd13-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fcd13-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd13-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcd13-112">Return value</span></span>

<span data-ttu-id="fcd13-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fcd13-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fcd13-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fcd13-114">Return code</span></span>                                                                               | <span data-ttu-id="fcd13-115">Description</span><span class="sxs-lookup"><span data-stu-id="fcd13-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fcd13-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fcd13-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fcd13-117">Succès</span><span class="sxs-lookup"><span data-stu-id="fcd13-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="fcd13-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="fcd13-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fcd13-119">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="fcd13-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fcd13-120">Notes</span><span class="sxs-lookup"><span data-stu-id="fcd13-120">Remarks</span></span>

<span data-ttu-id="fcd13-121">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="fcd13-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd13-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcd13-122">Requirements</span></span>



| <span data-ttu-id="fcd13-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcd13-123">Requirement</span></span> | <span data-ttu-id="fcd13-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcd13-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd13-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcd13-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fcd13-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcd13-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fcd13-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcd13-127">Library</span></span><br/> | <dl> <span data-ttu-id="fcd13-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fcd13-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd13-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcd13-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd13-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="fcd13-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




