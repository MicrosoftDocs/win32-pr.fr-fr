---
description: La méthode GetTransAtTime récupère la transition la plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'IAMTimelineTransable :: GetTransAtTime, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540072"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="74a42-103">IAMTimelineTransable :: GetTransAtTime, méthode</span><span class="sxs-lookup"><span data-stu-id="74a42-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="74a42-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="74a42-104">\[Deprecated.</span></span> <span data-ttu-id="74a42-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74a42-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74a42-106">La `GetTransAtTime` méthode récupère la transition la plus proche du temps spécifié, en fonction des conditions limites spécifiées.</span><span class="sxs-lookup"><span data-stu-id="74a42-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a42-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74a42-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="74a42-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74a42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a42-109">*ppObj* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="74a42-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74a42-110">Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la transition.</span><span class="sxs-lookup"><span data-stu-id="74a42-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="74a42-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="74a42-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="74a42-112">Heure à partir de laquelle commencer la recherche, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="74a42-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="74a42-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="74a42-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="74a42-114">Membre du type [**d' \_ \_ \_ indicateur de recherche DEXTERF Track**](dexterf-track-search-flags.md) qui spécifie les conditions limites pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="74a42-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a42-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74a42-115">Return value</span></span>

<span data-ttu-id="74a42-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="74a42-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="74a42-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="74a42-117">Return code</span></span>                                                                                  | <span data-ttu-id="74a42-118">Description</span><span class="sxs-lookup"><span data-stu-id="74a42-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="74a42-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="74a42-120">Aucune transition n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="74a42-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="74a42-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="74a42-122">La transition a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="74a42-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="74a42-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="74a42-124">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="74a42-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="74a42-125"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="74a42-126">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="74a42-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74a42-127">Notes</span><span class="sxs-lookup"><span data-stu-id="74a42-127">Remarks</span></span>

<span data-ttu-id="74a42-128">Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="74a42-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="74a42-129">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="74a42-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="74a42-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="74a42-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="74a42-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="74a42-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="74a42-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="74a42-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74a42-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74a42-133">Requirements</span></span>



| <span data-ttu-id="74a42-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74a42-134">Requirement</span></span> | <span data-ttu-id="74a42-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="74a42-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74a42-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="74a42-136">Header</span></span><br/>  | <dl> <span data-ttu-id="74a42-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="74a42-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="74a42-138">Library</span></span><br/> | <dl> <span data-ttu-id="74a42-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74a42-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74a42-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74a42-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a42-141">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="74a42-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="74a42-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="74a42-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




