---
description: La méthode InsertSpace fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'IAMTimelineTrack :: InsertSpace, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541269"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="ada49-103">IAMTimelineTrack :: InsertSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="ada49-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="ada49-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ada49-104">\[Deprecated.</span></span> <span data-ttu-id="ada49-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ada49-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ada49-106">La `InsertSpace` méthode fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux.</span><span class="sxs-lookup"><span data-stu-id="ada49-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada49-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ada49-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="ada49-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ada49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ada49-109">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="ada49-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ada49-110">Heure à laquelle créer le fractionnement, et le point de départ de l’espace inséré, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="ada49-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ada49-111">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="ada49-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ada49-112">Point de terminaison de l’espace inséré, en unités de 100 nanosecondes.</span><span class="sxs-lookup"><span data-stu-id="ada49-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ada49-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ada49-113">Return value</span></span>

<span data-ttu-id="ada49-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ada49-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ada49-115">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ada49-115">Possible return values include the following:</span></span>



| <span data-ttu-id="ada49-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ada49-116">Return code</span></span>                                                                                   | <span data-ttu-id="ada49-117">Description</span><span class="sxs-lookup"><span data-stu-id="ada49-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="ada49-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="ada49-119">Il n’y a aucun objet à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ada49-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="ada49-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ada49-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ada49-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ada49-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ada49-123">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="ada49-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="ada49-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ada49-125">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="ada49-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ada49-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ada49-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ada49-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="ada49-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ada49-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ada49-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ada49-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ada49-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ada49-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ada49-130">Requirements</span></span>



| <span data-ttu-id="ada49-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ada49-131">Requirement</span></span> | <span data-ttu-id="ada49-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ada49-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ada49-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="ada49-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ada49-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ada49-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ada49-135">Library</span></span><br/> | <dl> <span data-ttu-id="ada49-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ada49-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ada49-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ada49-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ada49-138">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="ada49-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ada49-139">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="ada49-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




