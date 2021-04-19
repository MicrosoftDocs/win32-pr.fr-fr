---
description: La méthode IsUsingTimeFormat détermine si un format d’heure spécifié est le format en cours d’utilisation.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Méthode CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528862"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="66ec5-103">Méthode CSourceSeeking. IsUsingTimeFormat</span><span class="sxs-lookup"><span data-stu-id="66ec5-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="66ec5-104">La `IsUsingTimeFormat` méthode détermine si un format d’heure spécifié est le format en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="66ec5-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ec5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66ec5-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="66ec5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66ec5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ec5-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="66ec5-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="66ec5-108">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="66ec5-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="66ec5-109">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="66ec5-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ec5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66ec5-110">Return value</span></span>

<span data-ttu-id="66ec5-111">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="66ec5-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="66ec5-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="66ec5-112">Return code</span></span>                                                                               | <span data-ttu-id="66ec5-113">Description</span><span class="sxs-lookup"><span data-stu-id="66ec5-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="66ec5-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec5-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="66ec5-115">Le format spécifié n’est pas le format actuel.</span><span class="sxs-lookup"><span data-stu-id="66ec5-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="66ec5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec5-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="66ec5-117">Le format spécifié est le format actuel.</span><span class="sxs-lookup"><span data-stu-id="66ec5-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="66ec5-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="66ec5-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="66ec5-119">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="66ec5-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="66ec5-120">Notes</span><span class="sxs-lookup"><span data-stu-id="66ec5-120">Remarks</span></span>

<span data-ttu-id="66ec5-121">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="66ec5-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="66ec5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66ec5-122">Requirements</span></span>



| <span data-ttu-id="66ec5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66ec5-123">Requirement</span></span> | <span data-ttu-id="66ec5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="66ec5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66ec5-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="66ec5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="66ec5-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66ec5-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="66ec5-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="66ec5-127">Library</span></span><br/> | <dl> <span data-ttu-id="66ec5-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="66ec5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ec5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ec5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ec5-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="66ec5-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




