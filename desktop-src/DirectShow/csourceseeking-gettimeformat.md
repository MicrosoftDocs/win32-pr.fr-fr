---
description: 'Méthode CSourceSeeking. GetTimeFormat : la méthode GetTimeFormat récupère le format d’heure actuel. Cette méthode implémente la méthode IMediaSeeking :: GetTimeFormat.'
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
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085217"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="e9ae3-104">Méthode CSourceSeeking. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e9ae3-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="e9ae3-105">La `GetTimeFormat` méthode récupère le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="e9ae3-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="e9ae3-106">Cette méthode implémente la méthode [**IMediaSeeking :: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="e9ae3-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ae3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ae3-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e9ae3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9ae3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ae3-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="e9ae3-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ae3-110">Pointeur vers une variable qui reçoit un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="e9ae3-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="e9ae3-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="e9ae3-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ae3-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e9ae3-112">Return value</span></span>

<span data-ttu-id="e9ae3-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9ae3-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="e9ae3-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e9ae3-114">Return code</span></span>                                                                               | <span data-ttu-id="e9ae3-115">Description</span><span class="sxs-lookup"><span data-stu-id="e9ae3-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="e9ae3-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae3-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e9ae3-117">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="e9ae3-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="e9ae3-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae3-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e9ae3-119">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="e9ae3-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e9ae3-120">Notes </span><span class="sxs-lookup"><span data-stu-id="e9ae3-120">Remarks</span></span>

<span data-ttu-id="e9ae3-121">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="e9ae3-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ae3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9ae3-122">Requirements</span></span>



| <span data-ttu-id="e9ae3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9ae3-123">Requirement</span></span> | <span data-ttu-id="e9ae3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9ae3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ae3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9ae3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9ae3-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae3-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9ae3-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9ae3-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9ae3-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ae3-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ae3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9ae3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ae3-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="e9ae3-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




