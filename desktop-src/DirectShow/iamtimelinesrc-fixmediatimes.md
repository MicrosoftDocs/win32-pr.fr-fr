---
description: La méthode FixMediaTimes arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie. En général, les applications n’ont pas besoin d’appeler cette méthode.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc :: FixMediaTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532710"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="56f58-104">IAMTimelineSrc :: FixMediaTimes, méthode</span><span class="sxs-lookup"><span data-stu-id="56f58-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="56f58-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="56f58-105">\[Deprecated.</span></span> <span data-ttu-id="56f58-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56f58-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56f58-107">La `FixMediaTimes` méthode arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie.</span><span class="sxs-lookup"><span data-stu-id="56f58-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="56f58-108">En général, les applications n’ont pas besoin d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="56f58-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f58-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56f58-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="56f58-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56f58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f58-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="56f58-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="56f58-112">Pointeur vers une variable qui contient l’heure de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="56f58-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="56f58-113">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="56f58-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="56f58-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="56f58-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="56f58-115">Pointeur vers une variable qui contient l’heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="56f58-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="56f58-116">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="56f58-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f58-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56f58-117">Return value</span></span>

<span data-ttu-id="56f58-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56f58-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56f58-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56f58-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56f58-120">Notes</span><span class="sxs-lookup"><span data-stu-id="56f58-120">Remarks</span></span>

<span data-ttu-id="56f58-121">Cette méthode est similaire à la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) , mais elle conserve le rapport d’origine des heures de temps et de chronologie des médias.</span><span class="sxs-lookup"><span data-stu-id="56f58-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="56f58-122">L’arrondi des heures à la limite de cadre la plus proche risque de déformer ce rapport.</span><span class="sxs-lookup"><span data-stu-id="56f58-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="56f58-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="56f58-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56f58-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="56f58-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56f58-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="56f58-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56f58-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56f58-126">Requirements</span></span>



| <span data-ttu-id="56f58-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56f58-127">Requirement</span></span> | <span data-ttu-id="56f58-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="56f58-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56f58-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="56f58-129">Header</span></span><br/>  | <dl> <span data-ttu-id="56f58-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56f58-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56f58-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="56f58-131">Library</span></span><br/> | <dl> <span data-ttu-id="56f58-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56f58-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56f58-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56f58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f58-134">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="56f58-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="56f58-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="56f58-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




