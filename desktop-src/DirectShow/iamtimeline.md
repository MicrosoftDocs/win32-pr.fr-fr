---
description: L’interface IAMTimeline fournit des méthodes pour manipuler la chronologie, l’objet central dans les services d’édition Microsoft DirectShow (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interface IAMTimeline (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540648"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="4711c-103">Interface IAMTimeline</span><span class="sxs-lookup"><span data-stu-id="4711c-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="4711c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="4711c-104">\[Deprecated.</span></span> <span data-ttu-id="4711c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4711c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4711c-106">L' `IAMTimeline` interface fournit des méthodes pour manipuler la chronologie, l’objet central dans les [services d’édition Microsoft DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="4711c-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="4711c-107">Une chronologie est une collection d’éléments chronologiques, tels que des clips vidéo, des clips audio, des effets et des transitions entre des éléments.</span><span class="sxs-lookup"><span data-stu-id="4711c-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="4711c-108">Le moteur de rendu utilise la chronologie pour créer un graphique de filtre, à partir duquel l’application peut générer la sortie rendue.</span><span class="sxs-lookup"><span data-stu-id="4711c-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="4711c-109">`IAMTimeline` effectue trois services de base.</span><span class="sxs-lookup"><span data-stu-id="4711c-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="4711c-110">Informatique</span><span class="sxs-lookup"><span data-stu-id="4711c-110">It</span></span>

-   <span data-ttu-id="4711c-111">Crée les objets dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="4711c-112">Agit comme un conteneur pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="4711c-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="4711c-113">Définit et récupère les paramètres généraux de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="4711c-114">Pour créer l’objet Timeline, appelez **CoCreateInstance** avec l’identificateur de classe CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="4711c-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="4711c-115">Membres</span><span class="sxs-lookup"><span data-stu-id="4711c-115">Members</span></span>

<span data-ttu-id="4711c-116">L’interface **IAMTimeline** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4711c-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4711c-117">**IAMTimeline** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4711c-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="4711c-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4711c-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4711c-119">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4711c-119">Methods</span></span>

<span data-ttu-id="4711c-120">L’interface **IAMTimeline** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4711c-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="4711c-121">Méthode</span><span class="sxs-lookup"><span data-stu-id="4711c-121">Method</span></span>                                                             | <span data-ttu-id="4711c-122">Description</span><span class="sxs-lookup"><span data-stu-id="4711c-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4711c-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="4711c-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="4711c-124">Ajoute un groupe à la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4711c-125">**ClearAllGroups**</span><span class="sxs-lookup"><span data-stu-id="4711c-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="4711c-126">Supprime tous les groupes de la chronologie, ainsi que tous les objets contenus dans ces groupes.</span><span class="sxs-lookup"><span data-stu-id="4711c-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="4711c-127">**CreateEmptyNode**</span><span class="sxs-lookup"><span data-stu-id="4711c-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="4711c-128">Crée un nouvel objet Timeline.</span><span class="sxs-lookup"><span data-stu-id="4711c-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4711c-129">**EffectsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4711c-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="4711c-130">Détermine si les effets sont activés.</span><span class="sxs-lookup"><span data-stu-id="4711c-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="4711c-131">**EnableEffects**</span><span class="sxs-lookup"><span data-stu-id="4711c-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="4711c-132">Active ou désactive tous les effets de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="4711c-133">**EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="4711c-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="4711c-134">Active ou désactive toutes les transitions dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="4711c-135">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="4711c-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="4711c-136">Récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.</span><span class="sxs-lookup"><span data-stu-id="4711c-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="4711c-137">**GetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4711c-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="4711c-138">Récupère l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="4711c-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="4711c-139">**GetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4711c-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="4711c-140">Récupère l’effet par défaut sous la forme d’une valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4711c-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="4711c-141">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4711c-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="4711c-142">Récupère la fréquence d’images de sortie par défaut, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4711c-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="4711c-143">**GetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4711c-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="4711c-144">Récupère la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="4711c-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4711c-145">**GetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4711c-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="4711c-146">Récupère la transition par défaut sous la forme d’une valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4711c-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="4711c-147">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="4711c-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="4711c-148">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4711c-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4711c-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="4711c-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="4711c-150">Récupère la durée de la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4711c-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="4711c-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="4711c-152">Récupère la durée de la chronologie sous la forme d’un **double**.</span><span class="sxs-lookup"><span data-stu-id="4711c-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="4711c-153">**GetGroup**</span><span class="sxs-lookup"><span data-stu-id="4711c-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="4711c-154">Récupère un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="4711c-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4711c-155">**GetGroupCount**</span><span class="sxs-lookup"><span data-stu-id="4711c-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="4711c-156">Récupère le nombre de groupes contenus dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="4711c-157">**GetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4711c-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="4711c-158">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4711c-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4711c-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="4711c-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="4711c-160">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4711c-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4711c-161">**RemGroupFromList**</span><span class="sxs-lookup"><span data-stu-id="4711c-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="4711c-162">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4711c-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="4711c-163">**SetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="4711c-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="4711c-164">Définit l’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="4711c-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="4711c-165">**SetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="4711c-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="4711c-166">Définit l’effet par défaut en tant que valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4711c-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4711c-167">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="4711c-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="4711c-168">Définit la fréquence d’images de sortie par défaut, en images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4711c-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="4711c-169">**SetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="4711c-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="4711c-170">Définit la transition par défaut.</span><span class="sxs-lookup"><span data-stu-id="4711c-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="4711c-171">**SetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="4711c-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="4711c-172">Définit la transition par défaut en tant que valeur BSTR.</span><span class="sxs-lookup"><span data-stu-id="4711c-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="4711c-173">**SetInsertMode**</span><span class="sxs-lookup"><span data-stu-id="4711c-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="4711c-174">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="4711c-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4711c-175">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="4711c-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="4711c-176">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="4711c-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="4711c-177">**TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="4711c-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="4711c-178">Détermine si les transitions sont activées.</span><span class="sxs-lookup"><span data-stu-id="4711c-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="4711c-179">**ValidateSourceNames**</span><span class="sxs-lookup"><span data-stu-id="4711c-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="4711c-180">Valide les noms de sources dans la chronologie.</span><span class="sxs-lookup"><span data-stu-id="4711c-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="4711c-181">Notes</span><span class="sxs-lookup"><span data-stu-id="4711c-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4711c-182">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="4711c-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4711c-183">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4711c-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4711c-184">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4711c-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4711c-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4711c-185">Requirements</span></span>



| <span data-ttu-id="4711c-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4711c-186">Requirement</span></span> | <span data-ttu-id="4711c-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="4711c-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4711c-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="4711c-188">Header</span></span><br/>  | <dl> <span data-ttu-id="4711c-189"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4711c-190">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4711c-190">Library</span></span><br/> | <dl> <span data-ttu-id="4711c-191"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4711c-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
