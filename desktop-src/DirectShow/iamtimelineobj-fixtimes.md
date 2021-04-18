---
description: La méthode FixTimes arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj :: FixTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526484"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="5ffc8-103">IAMTimelineObj :: FixTimes, méthode</span><span class="sxs-lookup"><span data-stu-id="5ffc8-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="5ffc8-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-104">\[Deprecated.</span></span> <span data-ttu-id="5ffc8-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5ffc8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5ffc8-106">La `FixTimes` méthode arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffc8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ffc8-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="5ffc8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ffc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ffc8-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="5ffc8-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5ffc8-110">Pointeur vers une variable qui contient l’heure de début, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="5ffc8-111">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="5ffc8-112">*pStop*</span><span class="sxs-lookup"><span data-stu-id="5ffc8-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="5ffc8-113">Pointeur vers une variable qui contient l’heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="5ffc8-114">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ffc8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ffc8-115">Return value</span></span>

<span data-ttu-id="5ffc8-116">Retourne S \_ OK en cas de réussite, ou E \_ NOTINTREE si l’objet ne fait pas partie d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ffc8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5ffc8-117">Remarks</span></span>

<span data-ttu-id="5ffc8-118">Pendant le rendu, DES arrondit les heures de début et de fin de l’objet à la limite d’image la plus proche.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="5ffc8-119">Toutefois, les ne remplacent pas les heures de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="5ffc8-120">Si vous modifiez la fréquence d’images de groupe, les temps arrondis sont toujours calculés à partir des heures d’origine.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="5ffc8-121">Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="5ffc8-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="5ffc8-122">Utilisez cette méthode pour déterminer les heures de démarrage et d’arrêt précises dans le projet rendu.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="5ffc8-123">Par exemple, vous devez rechercher les temps arrondis, plutôt que les heures de début et de fin d’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="5ffc8-124">Appelez [**IAMTimelineObj :: GetStartStop**](iamtimelineobj-getstartstop.md) pour obtenir les heures d’origine et passer ces valeurs à `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="5ffc8-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="5ffc8-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ffc8-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5ffc8-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5ffc8-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5ffc8-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ffc8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ffc8-128">Requirements</span></span>



| <span data-ttu-id="5ffc8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ffc8-129">Requirement</span></span> | <span data-ttu-id="5ffc8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ffc8-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffc8-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ffc8-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5ffc8-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc8-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5ffc8-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5ffc8-133">Library</span></span><br/> | <dl> <span data-ttu-id="5ffc8-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ffc8-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffc8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ffc8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffc8-136">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="5ffc8-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5ffc8-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="5ffc8-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




