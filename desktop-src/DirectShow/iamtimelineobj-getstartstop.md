---
description: La méthode GetStartStop récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj :: GetStartStop, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542321"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="fcd40-103">IAMTimelineObj :: GetStartStop, méthode</span><span class="sxs-lookup"><span data-stu-id="fcd40-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="fcd40-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="fcd40-104">\[Deprecated.</span></span> <span data-ttu-id="fcd40-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fcd40-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fcd40-106">La `GetStartStop` méthode récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fcd40-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd40-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcd40-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="fcd40-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcd40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd40-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="fcd40-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd40-110">Reçoit l’heure de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="fcd40-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="fcd40-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="fcd40-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="fcd40-112">Reçoit l’heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="fcd40-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd40-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcd40-113">Return value</span></span>

<span data-ttu-id="fcd40-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fcd40-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fcd40-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fcd40-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd40-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fcd40-116">Remarks</span></span>

<span data-ttu-id="fcd40-117">Les compositions, les groupes et les suivis ont toujours une heure de début égale à 0.</span><span class="sxs-lookup"><span data-stu-id="fcd40-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="fcd40-118">Pendant le rendu, DES arrondit les heures de début et de fin d’un objet à la limite d’image la plus proche.</span><span class="sxs-lookup"><span data-stu-id="fcd40-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="fcd40-119">Toutefois, les ne remplacent pas les heures de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fcd40-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="fcd40-120">Si vous modifiez la fréquence d’images de groupe, les temps arrondis sont toujours calculés à partir des heures d’origine.</span><span class="sxs-lookup"><span data-stu-id="fcd40-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="fcd40-121">Pour plus d’informations, retrouvez le [temps dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="fcd40-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="fcd40-122">Pour déterminer les heures de début et de fin dans le projet rendu, transmettez les valeurs retournées par `GetStartStop` à la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd40-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="fcd40-123">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="fcd40-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fcd40-124">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fcd40-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fcd40-125">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fcd40-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fcd40-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcd40-126">Requirements</span></span>



| <span data-ttu-id="fcd40-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcd40-127">Requirement</span></span> | <span data-ttu-id="fcd40-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcd40-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd40-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcd40-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fcd40-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd40-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fcd40-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcd40-131">Library</span></span><br/> | <dl> <span data-ttu-id="fcd40-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcd40-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd40-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcd40-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd40-134">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="fcd40-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="fcd40-135">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="fcd40-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




