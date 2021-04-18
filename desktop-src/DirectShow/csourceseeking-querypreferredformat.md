---
description: 'La méthode QueryPreferredFormat récupère le format d’heure préféré de l’objet. Cette méthode implémente la méthode IMediaSeeking :: QueryPreferredFormat.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Méthode CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533086"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="7094e-104">Méthode CSourceSeeking. QueryPreferredFormat</span><span class="sxs-lookup"><span data-stu-id="7094e-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="7094e-105">La `QueryPreferredFormat` méthode récupère le format d’heure préféré de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7094e-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="7094e-106">Cette méthode implémente la méthode [**IMediaSeeking :: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="7094e-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7094e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7094e-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7094e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7094e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7094e-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7094e-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7094e-110">Pointeur vers une variable qui reçoit un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="7094e-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="7094e-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7094e-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7094e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7094e-112">Return value</span></span>

<span data-ttu-id="7094e-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7094e-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="7094e-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7094e-114">Return code</span></span>                                                                               | <span data-ttu-id="7094e-115">Description</span><span class="sxs-lookup"><span data-stu-id="7094e-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="7094e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7094e-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7094e-117">Succès</span><span class="sxs-lookup"><span data-stu-id="7094e-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="7094e-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7094e-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7094e-119">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="7094e-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7094e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="7094e-120">Remarks</span></span>

<span data-ttu-id="7094e-121">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="7094e-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="7094e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7094e-122">Requirements</span></span>



| <span data-ttu-id="7094e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7094e-123">Requirement</span></span> | <span data-ttu-id="7094e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7094e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7094e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7094e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7094e-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7094e-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7094e-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7094e-127">Library</span></span><br/> | <dl> <span data-ttu-id="7094e-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7094e-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7094e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7094e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7094e-130">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="7094e-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




