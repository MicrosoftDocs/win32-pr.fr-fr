---
description: 'La méthode GetCurrentPosition récupère la position actuelle, par rapport à la durée totale du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Méthode CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523663"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="91cff-104">Méthode CPosPassThru. GetCurrentPosition</span><span class="sxs-lookup"><span data-stu-id="91cff-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="91cff-105">La `GetCurrentPosition` méthode récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="91cff-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="91cff-106">Cette méthode implémente la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .</span><span class="sxs-lookup"><span data-stu-id="91cff-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91cff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91cff-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="91cff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91cff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91cff-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="91cff-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="91cff-110">Pointeur vers une variable qui reçoit la position actuelle, en unités du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="91cff-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91cff-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91cff-111">Return value</span></span>

<span data-ttu-id="91cff-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91cff-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="91cff-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="91cff-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="91cff-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="91cff-114">Return code</span></span>                                                                               | <span data-ttu-id="91cff-115">Description</span><span class="sxs-lookup"><span data-stu-id="91cff-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="91cff-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91cff-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="91cff-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="91cff-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="91cff-118"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="91cff-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="91cff-119">La méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="91cff-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="91cff-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="91cff-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="91cff-121">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="91cff-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91cff-122">Notes</span><span class="sxs-lookup"><span data-stu-id="91cff-122">Remarks</span></span>

<span data-ttu-id="91cff-123">Cette méthode appelle la méthode [**CPosPassThru :: GetMediaTime**](cpospassthru-getmediatime.md) pour récupérer la position la plus récente.</span><span class="sxs-lookup"><span data-stu-id="91cff-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="91cff-124">Si **GetMediaTime** échoue, la méthode appelle **IMediaSeeking :: getCurrentPosition** sur l’épingle connecté.</span><span class="sxs-lookup"><span data-stu-id="91cff-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="91cff-125">La méthode **GetMediaTime** échoue par défaut dans la classe de base.</span><span class="sxs-lookup"><span data-stu-id="91cff-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="91cff-126">Si votre filtre met en cache la position actuelle, substituez **GetMediaTime** pour retourner la valeur mise en cache.</span><span class="sxs-lookup"><span data-stu-id="91cff-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="91cff-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91cff-127">Requirements</span></span>



| <span data-ttu-id="91cff-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91cff-128">Requirement</span></span> | <span data-ttu-id="91cff-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="91cff-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91cff-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91cff-130">Header</span></span><br/>  | <dl> <span data-ttu-id="91cff-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91cff-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91cff-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91cff-132">Library</span></span><br/> | <dl> <span data-ttu-id="91cff-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="91cff-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91cff-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91cff-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91cff-135">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="91cff-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




