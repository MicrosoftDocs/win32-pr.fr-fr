---
description: La méthode VTrackInsBefore insère une piste virtuelle dans la composition à la priorité spécifiée.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp :: VTrackInsBefore, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537850"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="3691e-103">IAMTimelineComp :: VTrackInsBefore, méthode</span><span class="sxs-lookup"><span data-stu-id="3691e-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="3691e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3691e-104">\[Deprecated.</span></span> <span data-ttu-id="3691e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3691e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3691e-106">La `VTrackInsBefore` méthode insère une piste virtuelle dans la composition à la priorité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3691e-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="3691e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3691e-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="3691e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3691e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3691e-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="3691e-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="3691e-110">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3691e-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="3691e-111">*Priorité*</span><span class="sxs-lookup"><span data-stu-id="3691e-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="3691e-112">Priorité à laquelle insérer la piste virtuelle, ou – 1 pour insérer la piste virtuelle à la fin de la liste de priorités.</span><span class="sxs-lookup"><span data-stu-id="3691e-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="3691e-113">La liste priorité détermine les clips visibles.</span><span class="sxs-lookup"><span data-stu-id="3691e-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="3691e-114">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="3691e-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3691e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3691e-115">Return value</span></span>

<span data-ttu-id="3691e-116">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="3691e-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="3691e-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3691e-117">Return code</span></span>                                                                                   | <span data-ttu-id="3691e-118">Description</span><span class="sxs-lookup"><span data-stu-id="3691e-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3691e-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3691e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3691e-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3691e-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3691e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3691e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3691e-122">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="3691e-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="3691e-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="3691e-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="3691e-124">L’objet n’est pas une piste virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3691e-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3691e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3691e-125">Remarks</span></span>

<span data-ttu-id="3691e-126">Chaque piste virtuelle de la composition a un niveau de priorité unique.</span><span class="sxs-lookup"><span data-stu-id="3691e-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="3691e-127">Les niveaux de priorité sont compris entre 0 et *n* -1, où *n* est le nombre de pistes virtuelles dans la composition.</span><span class="sxs-lookup"><span data-stu-id="3691e-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="3691e-128">Pour les groupes vidéo, une piste virtuelle masque toutes les pistes virtuelles avec un niveau de priorité inférieur, sauf dans les endroits où la piste est vide ou contient une transition.</span><span class="sxs-lookup"><span data-stu-id="3691e-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="3691e-129">Vous pouvez considérer les pistes virtuelles comme des couches dans la composition finale.</span><span class="sxs-lookup"><span data-stu-id="3691e-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="3691e-130">La piste 1 est superposée au-dessus de la piste 0, la piste 2 est superposée au-dessus de la piste 1, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3691e-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="3691e-131">Si vous spécifiez-1 pour le paramètre *Priority* , la piste virtuelle est insérée à la fin de la liste, avec une valeur de priorité plus élevée que les pistes existantes.</span><span class="sxs-lookup"><span data-stu-id="3691e-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="3691e-132">Si vous spécifiez une valeur de priorité qui existe déjà dans la composition, chaque piste avec une priorité égale ou supérieure se déplace vers le haut d’un niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="3691e-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="3691e-133">**Exemple**: Track A a la priorité 0 et la piste B a la priorité 1.</span><span class="sxs-lookup"><span data-stu-id="3691e-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="3691e-134">Si la piste C est insérée à la priorité 0, effectuez le suivi d’un déplacement vers la priorité 1, et la piste B passe à la priorité 2.</span><span class="sxs-lookup"><span data-stu-id="3691e-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="3691e-135">Si la priorité spécifiée est supérieure au nombre actuel de suivis dans la composition, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="3691e-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="3691e-136">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3691e-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3691e-137">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3691e-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3691e-138">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3691e-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3691e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3691e-139">Requirements</span></span>



| <span data-ttu-id="3691e-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3691e-140">Requirement</span></span> | <span data-ttu-id="3691e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="3691e-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3691e-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="3691e-142">Header</span></span><br/>  | <dl> <span data-ttu-id="3691e-143"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3691e-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3691e-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3691e-144">Library</span></span><br/> | <dl> <span data-ttu-id="3691e-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3691e-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3691e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3691e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3691e-147">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="3691e-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="3691e-148">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3691e-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




