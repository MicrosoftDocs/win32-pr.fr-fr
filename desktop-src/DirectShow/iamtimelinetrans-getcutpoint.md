---
description: La méthode GetCutPoint récupère le point de coupe.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'IAMTimelineTrans :: GetCutPoint, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545676"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="e2caf-103">IAMTimelineTrans :: GetCutPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="e2caf-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="e2caf-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e2caf-104">\[Deprecated.</span></span> <span data-ttu-id="e2caf-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2caf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e2caf-106">La `GetCutPoint` méthode récupère le point de coupe.</span><span class="sxs-lookup"><span data-stu-id="e2caf-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="e2caf-107">Si vous affichez une transition comme une coupe, le point de coupe est l’heure à laquelle la transition passe d’une source à la suivante.</span><span class="sxs-lookup"><span data-stu-id="e2caf-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="e2caf-108">Par défaut, cette valeur est le milieu de la transition.</span><span class="sxs-lookup"><span data-stu-id="e2caf-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="e2caf-109">Par exemple, dans une transition qui s’étend sur une seconde, le point de coupe par défaut est de 0,5 secondes dans la transition.</span><span class="sxs-lookup"><span data-stu-id="e2caf-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2caf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2caf-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="e2caf-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2caf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2caf-112">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="e2caf-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e2caf-113">Reçoit le point de coupe par rapport à l’heure de début de la transition, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="e2caf-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2caf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2caf-114">Return value</span></span>

<span data-ttu-id="e2caf-115">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2caf-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e2caf-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e2caf-116">Return code</span></span>                                                                               | <span data-ttu-id="e2caf-117">Description</span><span class="sxs-lookup"><span data-stu-id="e2caf-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2caf-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e2caf-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="e2caf-119">Le point de coupe n’a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="e2caf-119">The cut point was not set.</span></span> <span data-ttu-id="e2caf-120">La valeur retournée est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2caf-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="e2caf-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2caf-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e2caf-122">Le point de coupe a été défini sur une valeur autre que la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2caf-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="e2caf-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e2caf-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e2caf-124">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="e2caf-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="e2caf-125">Notes</span><span class="sxs-lookup"><span data-stu-id="e2caf-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2caf-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e2caf-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2caf-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e2caf-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e2caf-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e2caf-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e2caf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2caf-129">Requirements</span></span>



| <span data-ttu-id="e2caf-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2caf-130">Requirement</span></span> | <span data-ttu-id="e2caf-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2caf-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2caf-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2caf-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e2caf-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2caf-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e2caf-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2caf-134">Library</span></span><br/> | <dl> <span data-ttu-id="e2caf-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2caf-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2caf-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2caf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2caf-137">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="e2caf-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="e2caf-138">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="e2caf-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="e2caf-139">**IAMTimelineTrans::GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="e2caf-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="e2caf-140">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="e2caf-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="e2caf-141">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="e2caf-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




