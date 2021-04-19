---
description: La méthode SpliceWithNext joint l’objet source à un autre objet source.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc :: SpliceWithNext, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525152"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="aa0d6-103">IAMTimelineSrc :: SpliceWithNext, méthode</span><span class="sxs-lookup"><span data-stu-id="aa0d6-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="aa0d6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-104">\[Deprecated.</span></span> <span data-ttu-id="aa0d6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa0d6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aa0d6-106">La `SpliceWithNext` méthode joint l’objet source à un autre objet source.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0d6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa0d6-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="aa0d6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa0d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0d6-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="aa0d6-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="aa0d6-110">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source à joindre à la source actuelle.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0d6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa0d6-111">Return value</span></span>

<span data-ttu-id="aa0d6-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa0d6-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="aa0d6-113">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="aa0d6-113">Possible return values include the following:</span></span>



| <span data-ttu-id="aa0d6-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aa0d6-114">Return code</span></span>                                                                                   | <span data-ttu-id="aa0d6-115">Description</span><span class="sxs-lookup"><span data-stu-id="aa0d6-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa0d6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aa0d6-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="aa0d6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aa0d6-119">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="aa0d6-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="aa0d6-121">L’objet spécifié par le paramètre *pNext* n’est pas un objet source.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="aa0d6-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aa0d6-123">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="aa0d6-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="aa0d6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="aa0d6-124">Remarks</span></span>

<span data-ttu-id="aa0d6-125">Comme c’est actuellement le cas, cette méthode ignore les effets sur *pNext*.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="aa0d6-126">Pour que cette méthode aboutisse, *pNext* doit être une trame de correspondance de l’objet source actuel, définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="aa0d6-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="aa0d6-127">Il doit partager le même fichier source.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-127">It must share the same source file.</span></span>
-   <span data-ttu-id="aa0d6-128">L’heure de début du support doit être égale à l’heure d’arrêt du support de la source actuelle.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="aa0d6-129">La vitesse de lecture doit être la même.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-129">The playback rate must be the same.</span></span> <span data-ttu-id="aa0d6-130">La vitesse de lecture est la durée du support, divisée par la durée de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="aa0d6-131">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aa0d6-132">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa0d6-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aa0d6-133">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aa0d6-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa0d6-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa0d6-134">Requirements</span></span>



| <span data-ttu-id="aa0d6-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa0d6-135">Requirement</span></span> | <span data-ttu-id="aa0d6-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa0d6-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0d6-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa0d6-137">Header</span></span><br/>  | <dl> <span data-ttu-id="aa0d6-138"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aa0d6-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aa0d6-139">Library</span></span><br/> | <dl> <span data-ttu-id="aa0d6-140"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d6-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0d6-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa0d6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0d6-142">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="aa0d6-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="aa0d6-143">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="aa0d6-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




