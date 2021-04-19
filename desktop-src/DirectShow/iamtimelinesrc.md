---
description: L’interface IAMTimelineSrc fournit des méthodes pour manipuler et définir des propriétés sur les objets sources dans les services de modification DirectShow (DES).
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: Interface IAMTimelineSrc (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541267"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="17840-103">Interface IAMTimelineSrc</span><span class="sxs-lookup"><span data-stu-id="17840-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="17840-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="17840-104">\[Deprecated.</span></span> <span data-ttu-id="17840-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="17840-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17840-106">L' `IAMTimelineSrc` interface fournit des méthodes pour manipuler et définir des propriétés sur les objets sources dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="17840-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="17840-107">Un objet source représente un flux d’une source de média.</span><span class="sxs-lookup"><span data-stu-id="17840-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="17840-108">Vous pouvez utiliser une partie des données d’un fichier source en définissant les heures de démarrage et d’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="17840-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="17840-109">Ces valeurs spécifient le début et la fin de l’objet source, par rapport à la source du média d’origine.</span><span class="sxs-lookup"><span data-stu-id="17840-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="17840-110">Les temps de support peuvent différer de l’heure de début et de fin de l’objet sur la chronologie, ce qui permet une lecture rapide ou lente.</span><span class="sxs-lookup"><span data-stu-id="17840-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="17840-111">(Avec des sources audio, le décalage de hauteur se produit.)</span><span class="sxs-lookup"><span data-stu-id="17840-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="17840-112">Pour créer un objet source, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la valeur Timeline \_ principale \_ type \_ source.</span><span class="sxs-lookup"><span data-stu-id="17840-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="17840-113">Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l’interface **IAMTimelineSrc** .</span><span class="sxs-lookup"><span data-stu-id="17840-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="17840-114">Pour plus d’informations, consultez [construction d’une chronologie](constructing-a-timeline.md) et [utilisation de sources](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="17840-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="17840-115">Membres</span><span class="sxs-lookup"><span data-stu-id="17840-115">Members</span></span>

<span data-ttu-id="17840-116">L’interface **IAMTimelineSrc** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="17840-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17840-117">**IAMTimelineSrc** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17840-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="17840-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17840-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17840-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="17840-119">Methods</span></span>

<span data-ttu-id="17840-120">L’interface **IAMTimelineSrc** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="17840-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="17840-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="17840-121">Method</span></span>                                                    | <span data-ttu-id="17840-122">Description</span><span class="sxs-lookup"><span data-stu-id="17840-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17840-123">**FixMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="17840-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="17840-124">Arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche.</span><span class="sxs-lookup"><span data-stu-id="17840-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="17840-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="17840-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="17840-126">Arrondit les valeurs d’heure spécifiées, sous la forme de valeurs **REFTIME** , à la limite d’image la plus proche.</span><span class="sxs-lookup"><span data-stu-id="17840-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="17840-127">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="17840-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="17840-128">Récupère la fréquence d’images par défaut de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="17840-129">**GetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="17840-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="17840-130">Récupère la longueur du média de cet objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="17840-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="17840-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="17840-132">Récupère la longueur du média de cet objet source, sous la forme d’une valeur **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="17840-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="17840-133">**GetMediaName**</span><span class="sxs-lookup"><span data-stu-id="17840-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="17840-134">Récupère le nom du fichier source représenté par cet objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="17840-135">**GetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="17840-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="17840-136">Récupère les heures de démarrage et d’arrêt du média.</span><span class="sxs-lookup"><span data-stu-id="17840-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="17840-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="17840-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="17840-138">Récupère les heures de début et de fin du média, en tant que valeurs **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="17840-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="17840-139">**GetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="17840-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="17840-140">Récupère le numéro de flux actuel de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="17840-141">**GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="17840-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="17840-142">Récupère le mode stretch d’une source vidéo.</span><span class="sxs-lookup"><span data-stu-id="17840-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="17840-143">**IsNormalRate**</span><span class="sxs-lookup"><span data-stu-id="17840-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="17840-144">Indique si le clip sera lu à la vitesse de lecture normale.</span><span class="sxs-lookup"><span data-stu-id="17840-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="17840-145">**ModifyStopTime**</span><span class="sxs-lookup"><span data-stu-id="17840-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="17840-146">Définit l’heure d’arrêt, par rapport à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="17840-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="17840-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="17840-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="17840-148">Définit l’heure d’arrêt en tant que valeur **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="17840-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="17840-149">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="17840-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="17840-150">Définit la fréquence d’images par défaut de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="17840-151">**SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="17840-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="17840-152">Spécifie la durée du fichier source.</span><span class="sxs-lookup"><span data-stu-id="17840-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="17840-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="17840-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="17840-154">Spécifie la durée du fichier source, en tant que valeur **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="17840-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="17840-155">**SetMediaName**</span><span class="sxs-lookup"><span data-stu-id="17840-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="17840-156">Spécifie le nom du fichier source représenté par cet objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="17840-157">**SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="17840-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="17840-158">Définit l’heure de début et l’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="17840-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="17840-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="17840-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="17840-160">Définit l’heure de début et l’arrêt du support, en tant que valeurs **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="17840-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="17840-161">**SetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="17840-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="17840-162">Spécifie le flux à lire à partir du fichier source associé à cet objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="17840-163">**SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="17840-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="17840-164">Définit le mode d’étirement d’une source vidéo.</span><span class="sxs-lookup"><span data-stu-id="17840-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="17840-165">**SpliceWithNext**</span><span class="sxs-lookup"><span data-stu-id="17840-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="17840-166">Joint cet objet source à un autre objet source.</span><span class="sxs-lookup"><span data-stu-id="17840-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="17840-167">Notes</span><span class="sxs-lookup"><span data-stu-id="17840-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17840-168">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="17840-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17840-169">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="17840-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17840-170">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="17840-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17840-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17840-171">Requirements</span></span>



| <span data-ttu-id="17840-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17840-172">Requirement</span></span> | <span data-ttu-id="17840-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="17840-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17840-174">En-tête</span><span class="sxs-lookup"><span data-stu-id="17840-174">Header</span></span><br/>  | <dl> <span data-ttu-id="17840-175"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="17840-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17840-176">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17840-176">Library</span></span><br/> | <dl> <span data-ttu-id="17840-177"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17840-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
