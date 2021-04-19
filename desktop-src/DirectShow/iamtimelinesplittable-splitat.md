---
description: La méthode SplitAt fractionne l’objet à l’heure spécifiée.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable :: SplitAt, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537754"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="b491f-103">IAMTimelineSplittable :: SplitAt, méthode</span><span class="sxs-lookup"><span data-stu-id="b491f-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="b491f-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b491f-104">\[Deprecated.</span></span> <span data-ttu-id="b491f-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b491f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b491f-106">La `SplitAt` méthode fractionne l’objet à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b491f-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b491f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b491f-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="b491f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b491f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b491f-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="b491f-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="b491f-110">Heure à laquelle fractionner l’objet, par rapport au début de la chronologie, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="b491f-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b491f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b491f-111">Return value</span></span>

<span data-ttu-id="b491f-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b491f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b491f-113">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b491f-113">Possible values include the following:</span></span>



| <span data-ttu-id="b491f-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b491f-114">Return code</span></span>                                                                                   | <span data-ttu-id="b491f-115">Description</span><span class="sxs-lookup"><span data-stu-id="b491f-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b491f-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="b491f-117">Rien à fractionner.</span><span class="sxs-lookup"><span data-stu-id="b491f-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="b491f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b491f-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b491f-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="b491f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b491f-121">L’objet n’existe pas pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="b491f-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="b491f-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b491f-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="b491f-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b491f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b491f-124">Remarks</span></span>

<span data-ttu-id="b491f-125">Si vous fractionnez une source, un effet ou une transition, cette méthode crée un deuxième objet du même type.</span><span class="sxs-lookup"><span data-stu-id="b491f-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="b491f-126">L’objet d’origine est tronqué à l’heure de fractionnement spécifiée et le nouvel objet remplace la partie tronquée.</span><span class="sxs-lookup"><span data-stu-id="b491f-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="b491f-127">Le nouvel objet hérite de toutes les mêmes propriétés.</span><span class="sxs-lookup"><span data-stu-id="b491f-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="b491f-128">Dans un objet source, la méthode fractionne également tous les effets qui tombent sur l’heure de fractionnement.</span><span class="sxs-lookup"><span data-stu-id="b491f-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="b491f-129">L’appel de cette méthode sur une piste fractionne toutes les sources, effets et transitions contenus dans la piste à l’heure de fractionnement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b491f-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="b491f-130">Elle ne crée pas de deuxième piste. (Une piste commence à l’heure zéro et s’étend à l’infini.)</span><span class="sxs-lookup"><span data-stu-id="b491f-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="b491f-131">Pour une piste, si l’heure de fractionnement est postérieure à tout dans la piste, la méthode retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b491f-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="b491f-132">Pour tout autre objet, si l’heure de fractionnement n’est pas comprise dans l’objet, la méthode retourne E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b491f-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="b491f-133">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b491f-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b491f-134">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b491f-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b491f-135">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b491f-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b491f-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b491f-136">Requirements</span></span>



| <span data-ttu-id="b491f-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b491f-137">Requirement</span></span> | <span data-ttu-id="b491f-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b491f-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b491f-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b491f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="b491f-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b491f-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b491f-141">Library</span></span><br/> | <dl> <span data-ttu-id="b491f-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b491f-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b491f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b491f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b491f-144">**Interface IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="b491f-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="b491f-145">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b491f-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




