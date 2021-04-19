---
description: La méthode SetMediaTimes définit les heures de démarrage et d’arrêt du support.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc :: SetMediaTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539958"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="181dc-103">IAMTimelineSrc :: SetMediaTimes, méthode</span><span class="sxs-lookup"><span data-stu-id="181dc-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="181dc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="181dc-104">\[Deprecated.</span></span> <span data-ttu-id="181dc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="181dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="181dc-106">La `SetMediaTimes` méthode définit les heures de démarrage et d’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="181dc-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="181dc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="181dc-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="181dc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="181dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="181dc-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="181dc-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="181dc-110">Heure de début du média, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="181dc-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="181dc-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="181dc-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="181dc-112">Heure d’arrêt du support, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="181dc-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="181dc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="181dc-113">Return value</span></span>

<span data-ttu-id="181dc-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="181dc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="181dc-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="181dc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="181dc-116">Notes</span><span class="sxs-lookup"><span data-stu-id="181dc-116">Remarks</span></span>

<span data-ttu-id="181dc-117">Les heures de support sont les heures d’arrêt et de démarrage relatives au fichier multimédia d’origine.</span><span class="sxs-lookup"><span data-stu-id="181dc-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="181dc-118">Définissez toujours les temps de support lorsque vous ajoutez une source vidéo ou audio à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="181dc-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="181dc-119">Dans le cas contraire, des problèmes de rendu peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="181dc-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="181dc-120">L’heure d’arrêt doit être postérieure à l’heure de début.</span><span class="sxs-lookup"><span data-stu-id="181dc-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="181dc-121">Pour utiliser une image continue d’une source vidéo, définissez l’heure d’arrêt sur une valeur fractionnaire supérieure à l’heure de début, par exemple 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="181dc-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="181dc-122">La définition de la même valeur provoque une erreur de rendu.</span><span class="sxs-lookup"><span data-stu-id="181dc-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="181dc-123">Si la durée de la chronologie ne correspond pas à la durée du support, la source est étirée ou réduite en conséquence.</span><span class="sxs-lookup"><span data-stu-id="181dc-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="181dc-124">Cela provoque une lecture plus lente ou plus rapide du clip que la vitesse de création.</span><span class="sxs-lookup"><span data-stu-id="181dc-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="181dc-125">(Le décalage de la hauteur se produit dans une source audio.) Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="181dc-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="181dc-126">Vous pouvez spécifier la durée du fichier source en appelant la méthode [**SetMediaLength**](iamtimelinesrc-setmedialength.md) .</span><span class="sxs-lookup"><span data-stu-id="181dc-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="181dc-127">Si vous définissez une heure d’arrêt de support qui dépasse la durée, est tronque l’heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="181dc-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="181dc-128">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="181dc-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="181dc-129">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="181dc-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="181dc-130">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="181dc-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="181dc-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181dc-131">Requirements</span></span>



| <span data-ttu-id="181dc-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181dc-132">Requirement</span></span> | <span data-ttu-id="181dc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="181dc-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="181dc-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="181dc-134">Header</span></span><br/>  | <dl> <span data-ttu-id="181dc-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="181dc-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="181dc-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="181dc-136">Library</span></span><br/> | <dl> <span data-ttu-id="181dc-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="181dc-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181dc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181dc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181dc-139">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="181dc-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="181dc-140">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="181dc-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




