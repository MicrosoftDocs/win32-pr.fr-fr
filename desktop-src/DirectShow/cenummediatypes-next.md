---
description: 'La méthode suivante récupère un nombre spécifié de types de médias. Cette méthode implémente la méthode IEnumMediaTypes :: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Méthode CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530976"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="311c5-104">CEnumMediaTypes. Next, méthode</span><span class="sxs-lookup"><span data-stu-id="311c5-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="311c5-105">La `Next` méthode récupère un nombre spécifié de types de médias.</span><span class="sxs-lookup"><span data-stu-id="311c5-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="311c5-106">Cette méthode implémente la méthode [**IEnumMediaTypes :: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .</span><span class="sxs-lookup"><span data-stu-id="311c5-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="311c5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="311c5-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="311c5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="311c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311c5-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="311c5-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="311c5-110">Nombre de types de médias à récupérer.</span><span class="sxs-lookup"><span data-stu-id="311c5-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="311c5-111">*ppMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="311c5-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="311c5-112">Tableau de pointeurs vers des structures de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de taille *cPins*.</span><span class="sxs-lookup"><span data-stu-id="311c5-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="311c5-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="311c5-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="311c5-114">Pointeur vers une variable qui reçoit le nombre de types de médias que la méthode a retournés.</span><span class="sxs-lookup"><span data-stu-id="311c5-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="311c5-115">Peut avoir la **valeur null** si *cMediaTypes* est 1.</span><span class="sxs-lookup"><span data-stu-id="311c5-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311c5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="311c5-116">Return value</span></span>

<span data-ttu-id="311c5-117">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="311c5-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="311c5-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="311c5-118">Return code</span></span>                                                                                                | <span data-ttu-id="311c5-119">Description</span><span class="sxs-lookup"><span data-stu-id="311c5-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="311c5-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="311c5-121">N’a pas récupéré autant de types de média que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="311c5-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="311c5-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="311c5-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="311c5-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="311c5-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="311c5-125">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="311c5-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="311c5-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="311c5-127">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="311c5-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="311c5-128"><dt>**VFW \_ E \_ enum \_ non \_ \_ synchronisé**</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="311c5-129">L’état du pin a changé et est désormais incohérent avec l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="311c5-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="311c5-130">Notes</span><span class="sxs-lookup"><span data-stu-id="311c5-130">Remarks</span></span>

<span data-ttu-id="311c5-131">Si la méthode est réussie, le tableau spécifié par *ppMediaTypes* contient des pointeurs vers des \_ structures de type de média am \_ .</span><span class="sxs-lookup"><span data-stu-id="311c5-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="311c5-132">Le nombre de structures est égal à *\* pcFetched*.</span><span class="sxs-lookup"><span data-stu-id="311c5-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="311c5-133">Libérez chaque type de média en appelant la fonction [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="311c5-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="311c5-134">Cette méthode appelle la méthode [**CBasePin :: GetMediaType**](cbasepin-getmediatype.md) du pin pour récupérer les types de média.</span><span class="sxs-lookup"><span data-stu-id="311c5-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="311c5-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="311c5-135">Requirements</span></span>



| <span data-ttu-id="311c5-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="311c5-136">Requirement</span></span> | <span data-ttu-id="311c5-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="311c5-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="311c5-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="311c5-138">Header</span></span><br/>  | <dl> <span data-ttu-id="311c5-139"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="311c5-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="311c5-140">Library</span></span><br/> | <dl> <span data-ttu-id="311c5-141"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="311c5-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311c5-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="311c5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311c5-143">**CEnumMediaTypes, classe**</span><span class="sxs-lookup"><span data-stu-id="311c5-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




