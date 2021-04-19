---
description: La méthode GetNextSrc recherche dans le suivi la source suivante qui apparaît à l’heure spécifiée ou ultérieurement.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack :: GetNextSrc, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525371"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="42865-103">IAMTimelineTrack :: GetNextSrc, méthode</span><span class="sxs-lookup"><span data-stu-id="42865-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="42865-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="42865-104">\[Deprecated.</span></span> <span data-ttu-id="42865-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42865-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="42865-106">La `GetNextSrc` méthode recherche la source suivante qui apparaît à l’heure spécifiée ou une version ultérieure dans le suivi.</span><span class="sxs-lookup"><span data-stu-id="42865-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="42865-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42865-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="42865-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42865-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42865-109">*ppSrc* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="42865-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42865-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="42865-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="42865-111">*pInOut*</span><span class="sxs-lookup"><span data-stu-id="42865-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="42865-112">Pointeur vers une variable qui contient l’heure de début de la recherche, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="42865-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="42865-113">Si la méthode récupère une source, elle définit la valeur sur l’heure d’arrêt de la source.</span><span class="sxs-lookup"><span data-stu-id="42865-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="42865-114">Si la méthode ne récupère pas de source, la valeur devient non valide et l’application ne doit pas l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="42865-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42865-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42865-115">Return value</span></span>

<span data-ttu-id="42865-116">Retourne \_ la valeur OK si la méthode récupère une source, ou la \_ valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="42865-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="42865-117">Notes</span><span class="sxs-lookup"><span data-stu-id="42865-117">Remarks</span></span>

<span data-ttu-id="42865-118">Si l’heure spécifiée par *pInOut* se situe entre les heures de début et de fin d’une source, la méthode récupère cette source.</span><span class="sxs-lookup"><span data-stu-id="42865-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="42865-119">Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="42865-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="42865-120">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="42865-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="42865-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="42865-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="42865-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="42865-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="42865-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="42865-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42865-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42865-124">Requirements</span></span>



| <span data-ttu-id="42865-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42865-125">Requirement</span></span> | <span data-ttu-id="42865-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="42865-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42865-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="42865-127">Header</span></span><br/>  | <dl> <span data-ttu-id="42865-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="42865-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="42865-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42865-129">Library</span></span><br/> | <dl> <span data-ttu-id="42865-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42865-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42865-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42865-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42865-132">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="42865-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="42865-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="42865-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




