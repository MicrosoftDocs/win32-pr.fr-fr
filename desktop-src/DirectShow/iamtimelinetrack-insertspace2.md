---
description: 'La méthode InsertSpace2 fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux. Cette méthode est équivalente à IAMTimelineTrack :: InsertSpace, mais prend des valeurs REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'IAMTimelineTrack :: InsertSpace2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525171"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="a466c-104">IAMTimelineTrack :: InsertSpace2, méthode</span><span class="sxs-lookup"><span data-stu-id="a466c-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="a466c-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a466c-105">\[Deprecated.</span></span> <span data-ttu-id="a466c-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a466c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a466c-107">La `InsertSpace2` méthode fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux.</span><span class="sxs-lookup"><span data-stu-id="a466c-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="a466c-108">Cette méthode est équivalente à [**IAMTimelineTrack :: InsertSpace**](iamtimelinetrack-insertspace.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="a466c-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a466c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a466c-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="a466c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a466c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a466c-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="a466c-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a466c-112">Heure à laquelle le fractionnement est créé, et le point de départ de l’espace inséré, en secondes.</span><span class="sxs-lookup"><span data-stu-id="a466c-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="a466c-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="a466c-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a466c-114">Point de terminaison de l’espace inséré, en secondes.</span><span class="sxs-lookup"><span data-stu-id="a466c-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a466c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a466c-115">Return value</span></span>

<span data-ttu-id="a466c-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a466c-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a466c-117">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a466c-117">Possible return values include the following:</span></span>



| <span data-ttu-id="a466c-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a466c-118">Return code</span></span>                                                                                   | <span data-ttu-id="a466c-119">Description</span><span class="sxs-lookup"><span data-stu-id="a466c-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="a466c-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="a466c-121">Il n’y a aucun objet à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a466c-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="a466c-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a466c-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="a466c-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a466c-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a466c-125">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="a466c-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="a466c-126"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a466c-127">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="a466c-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a466c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a466c-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a466c-129">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="a466c-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a466c-130">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a466c-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a466c-131">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a466c-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a466c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a466c-132">Requirements</span></span>



| <span data-ttu-id="a466c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a466c-133">Requirement</span></span> | <span data-ttu-id="a466c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a466c-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a466c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="a466c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a466c-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a466c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a466c-137">Library</span></span><br/> | <dl> <span data-ttu-id="a466c-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a466c-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a466c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a466c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a466c-140">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="a466c-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="a466c-141">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="a466c-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




