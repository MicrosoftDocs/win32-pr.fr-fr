---
description: La méthode SetStartStop définit les heures de début et de fin de l’objet par rapport au parent de l’objet.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj :: SetStartStop, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526372"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="b70e8-103">IAMTimelineObj :: SetStartStop, méthode</span><span class="sxs-lookup"><span data-stu-id="b70e8-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="b70e8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b70e8-104">\[Deprecated.</span></span> <span data-ttu-id="b70e8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b70e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b70e8-106">La `SetStartStop` méthode définit les heures de début et de fin de l’objet par rapport au parent de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b70e8-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="b70e8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b70e8-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="b70e8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b70e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b70e8-109">*Start*</span><span class="sxs-lookup"><span data-stu-id="b70e8-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="b70e8-110">Nouvelle heure de début, en unités de 100 nanosecondes, ou-1 pour conserver l’heure de début existante.</span><span class="sxs-lookup"><span data-stu-id="b70e8-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="b70e8-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="b70e8-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="b70e8-112">Nouvelle heure d’arrêt, en unités de 100 nanosecondes, ou-1 pour conserver l’heure d’arrêt existante.</span><span class="sxs-lookup"><span data-stu-id="b70e8-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b70e8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b70e8-113">Return value</span></span>

<span data-ttu-id="b70e8-114">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="b70e8-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b70e8-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b70e8-115">Return code</span></span>                                                                                  | <span data-ttu-id="b70e8-116">Description</span><span class="sxs-lookup"><span data-stu-id="b70e8-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="b70e8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b70e8-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b70e8-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="b70e8-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="b70e8-120">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="b70e8-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="b70e8-121"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="b70e8-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="b70e8-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="b70e8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b70e8-123">Remarks</span></span>

<span data-ttu-id="b70e8-124">Les suivis, les compositions et les groupes n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b70e8-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="b70e8-125">Pour ces objets, l’heure de début est toujours égale à zéro et l’heure d’arrêt est l’heure d’arrêt maximale des objets qu’ils contiennent.</span><span class="sxs-lookup"><span data-stu-id="b70e8-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="b70e8-126">Ne définissez pas les heures qui se chevauchent sur les objets sources au sein d’une même piste. Cela peut entraîner des comportements non définis.</span><span class="sxs-lookup"><span data-stu-id="b70e8-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="b70e8-127">Pour les objets sources, les heures de début et de fin sont indépendantes des heures de début et de fin de support.</span><span class="sxs-lookup"><span data-stu-id="b70e8-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="b70e8-128">La modification d’une paire de valeurs ne modifie pas l’autre.</span><span class="sxs-lookup"><span data-stu-id="b70e8-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="b70e8-129">Pour définir les heures de début et de fin des médias, appelez la méthode [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="b70e8-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="b70e8-130">Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="b70e8-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="b70e8-131">Pour récupérer des transitions et des transitions de trame précises, définissez les paramètres de *démarrage* et d' *arrêt* sur les limites de cadre.</span><span class="sxs-lookup"><span data-stu-id="b70e8-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="b70e8-132">Vous pouvez utiliser la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) pour convertir une valeur d’heure dans la limite d’image la plus proche, ou utiliser la fonction suivante pour convertir le nombre de frames en temps de référence :</span><span class="sxs-lookup"><span data-stu-id="b70e8-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="b70e8-133">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b70e8-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b70e8-134">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b70e8-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b70e8-135">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b70e8-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b70e8-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b70e8-136">Requirements</span></span>



| <span data-ttu-id="b70e8-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b70e8-137">Requirement</span></span> | <span data-ttu-id="b70e8-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b70e8-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b70e8-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b70e8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b70e8-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b70e8-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b70e8-141">Library</span></span><br/> | <dl> <span data-ttu-id="b70e8-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b70e8-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b70e8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b70e8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b70e8-144">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="b70e8-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b70e8-145">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b70e8-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




