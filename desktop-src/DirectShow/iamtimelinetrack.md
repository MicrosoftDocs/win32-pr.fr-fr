---
description: L’interface IAMTimelineTrack fournit des méthodes pour manipuler les objets Track dans les services de modification DirectShow (DES). Une piste contient une liste de sources qui sont rendues dans la sortie finale.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Interface IAMTimelineTrack (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534901"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="9be88-103">Interface IAMTimelineTrack</span><span class="sxs-lookup"><span data-stu-id="9be88-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="9be88-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="9be88-104">\[Deprecated.</span></span> <span data-ttu-id="9be88-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9be88-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9be88-106">L' `IAMTimelineTrack` interface fournit des méthodes pour manipuler des objets *Track* dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="9be88-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="9be88-107">Une piste contient une liste de sources qui sont rendues dans la sortie finale.</span><span class="sxs-lookup"><span data-stu-id="9be88-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="9be88-108">Les sources au sein d’une même piste peuvent ne pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="9be88-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="9be88-109">Les pistes vidéo peuvent avoir des effets et des transitions.</span><span class="sxs-lookup"><span data-stu-id="9be88-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="9be88-110">Le moteur de rendu applique des effets avant d’appliquer des transitions.</span><span class="sxs-lookup"><span data-stu-id="9be88-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="9be88-111">Les pistes audio peuvent avoir des effets, mais pas des transitions.</span><span class="sxs-lookup"><span data-stu-id="9be88-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="9be88-112">Pour plus d’informations, consultez [le modèle Timeline](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="9be88-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="9be88-113">Pour créer un objet Track, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la valeur Timeline \_ de \_ type principal \_ Track.</span><span class="sxs-lookup"><span data-stu-id="9be88-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="9be88-114">Vous pouvez interroger le pointeur **IAMTimelineObj** retourné pour l' `IAMTimelineTrack` interface.</span><span class="sxs-lookup"><span data-stu-id="9be88-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="9be88-115">Membres</span><span class="sxs-lookup"><span data-stu-id="9be88-115">Members</span></span>

<span data-ttu-id="9be88-116">L’interface **IAMTimelineTrack** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9be88-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9be88-117">**IAMTimelineTrack** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9be88-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="9be88-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9be88-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9be88-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9be88-119">Methods</span></span>

<span data-ttu-id="9be88-120">L’interface **IAMTimelineTrack** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9be88-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="9be88-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="9be88-121">Method</span></span>                                                          | <span data-ttu-id="9be88-122">Description</span><span class="sxs-lookup"><span data-stu-id="9be88-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9be88-123">**AreYouBlank**</span><span class="sxs-lookup"><span data-stu-id="9be88-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="9be88-124">Détermine si la piste est vide (ne contient aucun objet source).</span><span class="sxs-lookup"><span data-stu-id="9be88-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="9be88-125">**GetNextSrc**</span><span class="sxs-lookup"><span data-stu-id="9be88-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="9be88-126">Recherche la source suivante qui s’affiche à l’heure spécifiée ou une version ultérieure dans le suivi.</span><span class="sxs-lookup"><span data-stu-id="9be88-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="9be88-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="9be88-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="9be88-128">Recherche dans la piste la source suivante qui apparaît à l’heure spécifiée ou ultérieurement, avec le donné comme valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9be88-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="9be88-129">**GetNextSrcEx**</span><span class="sxs-lookup"><span data-stu-id="9be88-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="9be88-130">Récupère la source suivante après la source spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9be88-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="9be88-131">**GetSourcesCount**</span><span class="sxs-lookup"><span data-stu-id="9be88-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="9be88-132">Récupère le nombre de sources dans la piste.</span><span class="sxs-lookup"><span data-stu-id="9be88-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="9be88-133">**GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="9be88-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="9be88-134">Récupère l’objet source le plus proche de l’heure spécifiée, en fonction des conditions limites spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9be88-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="9be88-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="9be88-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="9be88-136">Récupère l’objet source le plus proche de l’heure spécifiée, sous la forme d’une valeur [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9be88-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="9be88-137">**InsertSpace**</span><span class="sxs-lookup"><span data-stu-id="9be88-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="9be88-138">Fractionne tous les objets qui existent à l’heure spécifiée et insère un espace entre eux.</span><span class="sxs-lookup"><span data-stu-id="9be88-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="9be88-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="9be88-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="9be88-140">Fractionne tous les objets qui existent à l’heure spécifiée et insère de l’espace entre eux, à l’aide des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9be88-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="9be88-141">**MoveEverythingBy**</span><span class="sxs-lookup"><span data-stu-id="9be88-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="9be88-142">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9be88-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="9be88-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="9be88-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="9be88-144">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9be88-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="9be88-145">**SrcAdd**</span><span class="sxs-lookup"><span data-stu-id="9be88-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="9be88-146">Ajoute une source à la piste.</span><span class="sxs-lookup"><span data-stu-id="9be88-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="9be88-147">**ZeroBetween**</span><span class="sxs-lookup"><span data-stu-id="9be88-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="9be88-148">Supprime tous les éléments de la piste entre les heures spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9be88-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="9be88-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="9be88-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="9be88-150">Supprime tous les éléments de la piste entre les heures spécifiées, en fonction des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9be88-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="9be88-151">Notes</span><span class="sxs-lookup"><span data-stu-id="9be88-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9be88-152">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="9be88-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9be88-153">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9be88-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9be88-154">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9be88-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9be88-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9be88-155">Requirements</span></span>



| <span data-ttu-id="9be88-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9be88-156">Requirement</span></span> | <span data-ttu-id="9be88-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="9be88-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be88-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="9be88-158">Header</span></span><br/>  | <dl> <span data-ttu-id="9be88-159"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be88-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9be88-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9be88-160">Library</span></span><br/> | <dl> <span data-ttu-id="9be88-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9be88-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
