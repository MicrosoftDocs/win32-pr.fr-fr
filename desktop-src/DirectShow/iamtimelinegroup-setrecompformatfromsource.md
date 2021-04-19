---
description: La méthode SetRecompFormatFromSource définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'IAMTimelineGroup :: SetRecompFormatFromSource, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544042"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a><span data-ttu-id="d0c4d-103">IAMTimelineGroup :: SetRecompFormatFromSource, méthode</span><span class="sxs-lookup"><span data-stu-id="d0c4d-103">IAMTimelineGroup::SetRecompFormatFromSource method</span></span>

> [!Note]  
> <span data-ttu-id="d0c4d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-104">\[Deprecated.</span></span> <span data-ttu-id="d0c4d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0c4d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0c4d-106">La `SetRecompFormatFromSource` méthode définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-106">The `SetRecompFormatFromSource` method sets the video recompression format using the compression format from a source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c4d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c4d-107">Syntax</span></span>


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="d0c4d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c4d-109">*pSource*</span><span class="sxs-lookup"><span data-stu-id="d0c4d-109">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c4d-110">Pointeur vers l’interface [**IAMTimelineSrc**](iamtimelinesrc.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-110">Pointer to the [**IAMTimelineSrc**](iamtimelinesrc.md) interface of the source object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c4d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0c4d-111">Return value</span></span>

<span data-ttu-id="d0c4d-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0c4d-112">Returns an **HRESULT** values.</span></span> <span data-ttu-id="d0c4d-113">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-113">Possible values include the following.</span></span>



| <span data-ttu-id="d0c4d-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d0c4d-114">Return code</span></span>                                                                                             | <span data-ttu-id="d0c4d-115">Description</span><span class="sxs-lookup"><span data-stu-id="d0c4d-115">Description</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d0c4d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="d0c4d-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-117">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d0c4d-118"><dt>**E \_ aucune \_ chronologie**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-118"><dt>**E\_NO\_TIMELINE**</dt></span></span> </dl>          | <span data-ttu-id="d0c4d-119">Le groupe n’est pas dans une chronologie.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-119">The group is not within a timeline.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="d0c4d-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="d0c4d-121">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-121">Insufficient memory.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d0c4d-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-122"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="d0c4d-123">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="d0c4d-123">**NULL** pointer argument.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="d0c4d-124"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-124"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="d0c4d-125">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-125">Invalid media type.</span></span> <span data-ttu-id="d0c4d-126">Le groupe n’est pas un groupe vidéo ou le fichier source n’a pas de flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-126">The group is not a video group, or the source file has no video stream.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0c4d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d0c4d-127">Remarks</span></span>

<span data-ttu-id="d0c4d-128">Cette méthode recherche le fichier source associé à *pSource*, récupère le type de média du premier flux vidéo dans le fichier et définit le format de compression de groupe à l’aide de ce type.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-128">This method finds the source file associated with *pSource*, retrieves the media type of the first video stream in the file, and sets the group compression format using that type.</span></span> <span data-ttu-id="d0c4d-129">Pour plus d’informations sur les formats de compression, consultez [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span><span class="sxs-lookup"><span data-stu-id="d0c4d-129">For more information about compression formats, see [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0c4d-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0c4d-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0c4d-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0c4d-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0c4d-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0c4d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0c4d-133">Requirements</span></span>



| <span data-ttu-id="d0c4d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0c4d-134">Requirement</span></span> | <span data-ttu-id="d0c4d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0c4d-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c4d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0c4d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c4d-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0c4d-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0c4d-138">Library</span></span><br/> | <dl> <span data-ttu-id="d0c4d-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0c4d-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c4d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c4d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c4d-141">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="d0c4d-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d0c4d-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="d0c4d-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




