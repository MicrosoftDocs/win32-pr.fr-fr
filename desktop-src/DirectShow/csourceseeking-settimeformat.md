---
description: 'Méthode CSourceSeeking. SetTimeFormat : la méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode IMediaSeeking :: SetTimeFormat.'
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Méthode CSourceSeeking. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085197"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="22bf9-104">Méthode CSourceSeeking. SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="22bf9-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="22bf9-105">La `SetTimeFormat` méthode définit le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="22bf9-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="22bf9-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="22bf9-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22bf9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22bf9-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="22bf9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22bf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22bf9-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="22bf9-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="22bf9-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="22bf9-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="22bf9-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="22bf9-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22bf9-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="22bf9-112">Return value</span></span>

<span data-ttu-id="22bf9-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22bf9-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="22bf9-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="22bf9-114">Return code</span></span>                                                                                  | <span data-ttu-id="22bf9-115">Description</span><span class="sxs-lookup"><span data-stu-id="22bf9-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="22bf9-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22bf9-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="22bf9-117">Réussite.</span><span class="sxs-lookup"><span data-stu-id="22bf9-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="22bf9-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="22bf9-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="22bf9-119">Le format spécifié n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22bf9-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="22bf9-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="22bf9-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="22bf9-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="22bf9-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="22bf9-122">Notes </span><span class="sxs-lookup"><span data-stu-id="22bf9-122">Remarks</span></span>

<span data-ttu-id="22bf9-123">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="22bf9-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="22bf9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22bf9-124">Requirements</span></span>



| <span data-ttu-id="22bf9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22bf9-125">Requirement</span></span> | <span data-ttu-id="22bf9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="22bf9-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22bf9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="22bf9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="22bf9-128"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22bf9-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22bf9-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22bf9-129">Library</span></span><br/> | <dl> <span data-ttu-id="22bf9-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22bf9-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22bf9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22bf9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22bf9-132">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="22bf9-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




