---
description: 'L’interface IAMTimelineGroup définit et récupère les propriétés des groupes dans les services d’édition DirectShow (DES). Un groupe contient une ou plusieurs pistes et, éventuellement, une ou plusieurs compositions, qui à leur tour contiennent des éléments sources d’un type uniforme, tels que des vidéos ou des données audio. Les groupes sont les compositions les plus principales dans une chronologie et exposent également l’interface IAMTimelineComp. Une chronologie peut contenir plusieurs groupes. Chaque groupe a les attributs suivants. Type de média associé. Fréquence d’images à laquelle le groupe effectue le rendu, en images par seconde (FPS). Toutes les modifications se produisent à un moment arrondi à la limite d’image la plus proche, comme défini par le paramètre FPS du groupe. Niveau de priorité, pour l’écriture de fichiers avec plusieurs flux du même type de média (par exemple, un fichier AVI en deux vidéos). Pour créer un objet de groupe, appelez IAMTimeline :: CreateEmptyNode avec le \_ groupe de types major de la valeur Timeline \_ \_ . Vous pouvez interroger le pointeur IAMTimelineObj retourné pour l’interface IAMTimelineGroup.'
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: Interface IAMTimelineGroup (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540096"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="741a4-107">Interface IAMTimelineGroup</span><span class="sxs-lookup"><span data-stu-id="741a4-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="741a4-108">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="741a4-108">\[Deprecated.</span></span> <span data-ttu-id="741a4-109">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="741a4-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="741a4-110">L' `IAMTimelineGroup` interface définit et récupère des propriétés sur des groupes dans les [services d’édition DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="741a4-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="741a4-111">Un groupe contient une ou plusieurs pistes et, éventuellement, une ou plusieurs compositions, qui à leur tour contiennent des éléments sources d’un type uniforme, tels que des vidéos ou des données audio.</span><span class="sxs-lookup"><span data-stu-id="741a4-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="741a4-112">Les groupes sont les compositions les plus principales dans une chronologie et exposent également l’interface [**IAMTimelineComp**](iamtimelinecomp.md) .</span><span class="sxs-lookup"><span data-stu-id="741a4-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="741a4-113">Une chronologie peut contenir plusieurs groupes.</span><span class="sxs-lookup"><span data-stu-id="741a4-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="741a4-114">Chaque groupe a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="741a4-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="741a4-115">Type de média associé.</span><span class="sxs-lookup"><span data-stu-id="741a4-115">An associated media type.</span></span>
-   <span data-ttu-id="741a4-116">Fréquence d’images à laquelle le groupe effectue le rendu, en images par seconde (FPS).</span><span class="sxs-lookup"><span data-stu-id="741a4-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="741a4-117">Toutes les modifications se produisent à un moment arrondi à la limite d’image la plus proche, comme défini par le paramètre FPS du groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="741a4-118">Niveau de priorité, pour l’écriture de fichiers avec plusieurs flux du même type de média (par exemple, un fichier AVI en deux vidéos).</span><span class="sxs-lookup"><span data-stu-id="741a4-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="741a4-119">Pour créer un objet de groupe, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec le \_ groupe de types major de la valeur Timeline \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="741a4-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="741a4-120">Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l’interface **IAMTimelineGroup** .</span><span class="sxs-lookup"><span data-stu-id="741a4-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="741a4-121">Membres</span><span class="sxs-lookup"><span data-stu-id="741a4-121">Members</span></span>

<span data-ttu-id="741a4-122">L’interface **IAMTimelineGroup** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="741a4-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="741a4-123">**IAMTimelineGroup** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="741a4-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="741a4-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="741a4-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="741a4-125">Méthodes</span><span class="sxs-lookup"><span data-stu-id="741a4-125">Methods</span></span>

<span data-ttu-id="741a4-126">L’interface **IAMTimelineGroup** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="741a4-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="741a4-127">Méthode</span><span class="sxs-lookup"><span data-stu-id="741a4-127">Method</span></span>                                                                            | <span data-ttu-id="741a4-128">Description</span><span class="sxs-lookup"><span data-stu-id="741a4-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="741a4-129">**ClearRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="741a4-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="741a4-130">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="741a4-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="741a4-131">**GetGroupName**</span><span class="sxs-lookup"><span data-stu-id="741a4-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="741a4-132">Récupère le nom défini par l’application du groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="741a4-133">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="741a4-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="741a4-134">Récupère le type de média non compressé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="741a4-135">**GetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="741a4-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="741a4-136">Récupère le nombre d’images rendues à l’avance pendant la préversion.</span><span class="sxs-lookup"><span data-stu-id="741a4-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="741a4-137">**GetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="741a4-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="741a4-138">Récupère la fréquence d’images de sortie de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="741a4-139">**GetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="741a4-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="741a4-140">Récupère le mode Aperçu pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="741a4-141">**GetPriority,**</span><span class="sxs-lookup"><span data-stu-id="741a4-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="741a4-142">Récupère la priorité du groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="741a4-143">**GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="741a4-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="741a4-144">Récupère le format de compression actuel pour la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="741a4-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="741a4-145">**GetTimeline**</span><span class="sxs-lookup"><span data-stu-id="741a4-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="741a4-146">Récupère la chronologie à laquelle appartient ce groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="741a4-147">**IsRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="741a4-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="741a4-148">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="741a4-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="741a4-149">**IsSmartRecompressFormatSet**</span><span class="sxs-lookup"><span data-stu-id="741a4-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="741a4-150">Détermine si un format de compression intelligente a été défini pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="741a4-151">**SetGroupName**</span><span class="sxs-lookup"><span data-stu-id="741a4-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="741a4-152">Définit le nom défini par l’application du groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="741a4-153">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="741a4-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="741a4-154">Définit le type de média non compressé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="741a4-155">**SetMediaTypeForVB**</span><span class="sxs-lookup"><span data-stu-id="741a4-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="741a4-156">Spécifie le type de média du groupe pour les clients Automation.</span><span class="sxs-lookup"><span data-stu-id="741a4-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="741a4-157">**SetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="741a4-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="741a4-158">Spécifie le nombre d’images rendues à l’avance pendant la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="741a4-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="741a4-159">**SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="741a4-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="741a4-160">Définit la fréquence d’images de sortie non compressées pour ce groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="741a4-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="741a4-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="741a4-162">Définit le mode Aperçu pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="741a4-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="741a4-163">**SetRecompFormatFromSource**</span><span class="sxs-lookup"><span data-stu-id="741a4-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="741a4-164">Définit le format de recompression vidéo à l’aide du format de compression d’un fichier source.</span><span class="sxs-lookup"><span data-stu-id="741a4-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="741a4-165">**SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="741a4-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="741a4-166">Spécifie un format de compression à utiliser pour la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="741a4-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="741a4-167">**SetTimeline**</span><span class="sxs-lookup"><span data-stu-id="741a4-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="741a4-168">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="741a4-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="741a4-169">Notes</span><span class="sxs-lookup"><span data-stu-id="741a4-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="741a4-170">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="741a4-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="741a4-171">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="741a4-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="741a4-172">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="741a4-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="741a4-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="741a4-173">Requirements</span></span>



| <span data-ttu-id="741a4-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="741a4-174">Requirement</span></span> | <span data-ttu-id="741a4-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="741a4-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="741a4-176">En-tête</span><span class="sxs-lookup"><span data-stu-id="741a4-176">Header</span></span><br/>  | <dl> <span data-ttu-id="741a4-177"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="741a4-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="741a4-178">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="741a4-178">Library</span></span><br/> | <dl> <span data-ttu-id="741a4-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="741a4-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
