---
description: 'La méthode IsFormatSupported détermine si un format d’heure spécifié est pris en charge. Cette méthode implémente la méthode IMediaSeeking :: IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Méthode CSourceSeeking. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540528"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="22e3f-104">Méthode CSourceSeeking. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="22e3f-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="22e3f-105">La `IsFormatSupported` méthode détermine si un format d’heure spécifié est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22e3f-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="22e3f-106">Cette méthode implémente la méthode [**IMediaSeeking :: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="22e3f-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e3f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22e3f-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="22e3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22e3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e3f-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="22e3f-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="22e3f-110">Pointeur vers un GUID de format d’heure.</span><span class="sxs-lookup"><span data-stu-id="22e3f-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="22e3f-111">Consultez [**GUID de format d’heure**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="22e3f-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e3f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22e3f-112">Return value</span></span>

<span data-ttu-id="22e3f-113">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22e3f-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="22e3f-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="22e3f-114">Return code</span></span>                                                                               | <span data-ttu-id="22e3f-115">Description</span><span class="sxs-lookup"><span data-stu-id="22e3f-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="22e3f-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="22e3f-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="22e3f-117">Le format n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22e3f-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="22e3f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22e3f-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="22e3f-119">Le format est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22e3f-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="22e3f-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="22e3f-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="22e3f-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="22e3f-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="22e3f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="22e3f-122">Remarks</span></span>

<span data-ttu-id="22e3f-123">Le seul format d’heure pris en charge par la classe de base est le format d’heure du \_ \_ \_ temps de support (unités de 100 nanosecondes).</span><span class="sxs-lookup"><span data-stu-id="22e3f-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="22e3f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22e3f-124">Requirements</span></span>



| <span data-ttu-id="22e3f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22e3f-125">Requirement</span></span> | <span data-ttu-id="22e3f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="22e3f-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22e3f-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="22e3f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="22e3f-128"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22e3f-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="22e3f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="22e3f-129">Library</span></span><br/> | <dl> <span data-ttu-id="22e3f-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="22e3f-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e3f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22e3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e3f-132">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="22e3f-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




