---
description: 'La méthode SetTimeFormat définit le format d’heure. Cette méthode implémente la méthode IMediaSeeking :: SetTimeFormat.'
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
ms.openlocfilehash: 61ab0cdf7c954e0fa5f370127f00529bb9ef7b16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537919"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="80a39-104">Méthode CSourceSeeking. SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="80a39-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="80a39-105">La `SetTimeFormat` méthode définit le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="80a39-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="80a39-106">Cette méthode implémente la méthode [**IMediaSeeking :: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="80a39-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a39-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80a39-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="80a39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80a39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a39-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="80a39-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="80a39-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="80a39-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="80a39-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="80a39-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a39-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80a39-112">Return value</span></span>

<span data-ttu-id="80a39-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="80a39-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="80a39-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="80a39-114">Return code</span></span>                                                                                  | <span data-ttu-id="80a39-115">Description</span><span class="sxs-lookup"><span data-stu-id="80a39-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="80a39-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80a39-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="80a39-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="80a39-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="80a39-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="80a39-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="80a39-119">Le format spécifié n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="80a39-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="80a39-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="80a39-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="80a39-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="80a39-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="80a39-122">Notes</span><span class="sxs-lookup"><span data-stu-id="80a39-122">Remarks</span></span>

<span data-ttu-id="80a39-123">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="80a39-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="80a39-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80a39-124">Requirements</span></span>



| <span data-ttu-id="80a39-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80a39-125">Requirement</span></span> | <span data-ttu-id="80a39-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="80a39-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80a39-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="80a39-127">Header</span></span><br/>  | <dl> <span data-ttu-id="80a39-128"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80a39-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80a39-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80a39-129">Library</span></span><br/> | <dl> <span data-ttu-id="80a39-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="80a39-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a39-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80a39-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a39-132">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="80a39-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




