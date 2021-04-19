---
description: La méthode ModifyStopTime définit l’heure d’arrêt, par rapport à la chronologie.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc :: ModifyStopTime, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533458"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="094fd-103">IAMTimelineSrc :: ModifyStopTime, méthode</span><span class="sxs-lookup"><span data-stu-id="094fd-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="094fd-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="094fd-104">\[Deprecated.</span></span> <span data-ttu-id="094fd-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="094fd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="094fd-106">La `ModifyStopTime` méthode définit l’heure d’arrêt, par rapport à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="094fd-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="094fd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="094fd-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="094fd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="094fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="094fd-109">*Stop*</span><span class="sxs-lookup"><span data-stu-id="094fd-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="094fd-110">Nouvelle heure d’arrêt, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="094fd-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="094fd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="094fd-111">Return value</span></span>

<span data-ttu-id="094fd-112">Retourne S \_ OK ou E \_ INVALIDARG si l’heure spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="094fd-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="094fd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="094fd-113">Remarks</span></span>

<span data-ttu-id="094fd-114">Cette méthode équivaut à appeler [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) avec l’heure de début d’origine et une nouvelle heure d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="094fd-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="094fd-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="094fd-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="094fd-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="094fd-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="094fd-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="094fd-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="094fd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="094fd-118">Requirements</span></span>



| <span data-ttu-id="094fd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="094fd-119">Requirement</span></span> | <span data-ttu-id="094fd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="094fd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="094fd-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="094fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="094fd-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="094fd-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="094fd-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="094fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="094fd-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="094fd-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="094fd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="094fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094fd-126">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="094fd-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="094fd-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="094fd-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




