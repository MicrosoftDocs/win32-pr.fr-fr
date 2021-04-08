---
title: Controls (objet)
description: L’objet Controls permet de manipuler la lecture des médias à l’aide des propriétés et méthodes suivantes.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Contrôle l’objet Windows Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678833"
---
# <a name="controls-object"></a><span data-ttu-id="022c1-104">Controls (objet)</span><span class="sxs-lookup"><span data-stu-id="022c1-104">Controls Object</span></span>

<span data-ttu-id="022c1-105">L’objet **Controls** permet de manipuler la lecture des médias à l’aide des propriétés et méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="022c1-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="022c1-106">L’objet **Controls** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="022c1-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="022c1-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="022c1-107">Property</span></span>                                                            | <span data-ttu-id="022c1-108">Description</span><span class="sxs-lookup"><span data-stu-id="022c1-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="022c1-109">audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="022c1-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="022c1-110">Récupère le nombre de langues audio prises en charge.</span><span class="sxs-lookup"><span data-stu-id="022c1-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="022c1-111">currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="022c1-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="022c1-112">Spécifie ou récupère l’identificateur de paramètres régionaux (LCID) de la langue audio pour la lecture</span><span class="sxs-lookup"><span data-stu-id="022c1-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="022c1-113">currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="022c1-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="022c1-114">Spécifie ou récupère l’index de base un qui correspond au langage audio pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="022c1-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="022c1-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="022c1-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="022c1-116">Spécifie ou récupère l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="022c1-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="022c1-117">currentMarker</span><span class="sxs-lookup"><span data-stu-id="022c1-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="022c1-118">Spécifie ou récupère le numéro de marqueur actuel.</span><span class="sxs-lookup"><span data-stu-id="022c1-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="022c1-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="022c1-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="022c1-120">Spécifie ou récupère, en secondes, la position actuelle dans l’élément multimédia à partir du début.</span><span class="sxs-lookup"><span data-stu-id="022c1-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="022c1-121">currentPositionString</span><span class="sxs-lookup"><span data-stu-id="022c1-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="022c1-122">Récupère la position actuelle dans l’élément multimédia sous la forme d’une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="022c1-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="022c1-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="022c1-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="022c1-124">Spécifie ou récupère la position actuelle dans l’élément multimédia en cours à l’aide d’un format de code temporel.</span><span class="sxs-lookup"><span data-stu-id="022c1-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="022c1-125">Cette propriété prend actuellement en charge le code de temps SMPTE.</span><span class="sxs-lookup"><span data-stu-id="022c1-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="022c1-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="022c1-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="022c1-127">Récupère une valeur indiquant si un type d’informations spécifié est disponible ou si une action donnée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="022c1-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="022c1-128">L’objet **Controls** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="022c1-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="022c1-129">Méthode</span><span class="sxs-lookup"><span data-stu-id="022c1-129">Method</span></span>                                                                  | <span data-ttu-id="022c1-130">Description</span><span class="sxs-lookup"><span data-stu-id="022c1-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="022c1-131">fastForward</span><span class="sxs-lookup"><span data-stu-id="022c1-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="022c1-132">Démarre la lecture rapide de l’élément multimédia dans le sens avant.</span><span class="sxs-lookup"><span data-stu-id="022c1-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="022c1-133">fastReverse</span><span class="sxs-lookup"><span data-stu-id="022c1-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="022c1-134">Démarre la lecture rapide de l’élément multimédia dans le sens inverse.</span><span class="sxs-lookup"><span data-stu-id="022c1-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="022c1-135">getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="022c1-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="022c1-136">Récupère la description de la langue audio correspondant à l’index de base 1 spécifié.</span><span class="sxs-lookup"><span data-stu-id="022c1-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="022c1-137">getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="022c1-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="022c1-138">Récupère le LCID pour un index de langue audio spécifié.</span><span class="sxs-lookup"><span data-stu-id="022c1-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="022c1-139">getLanguageName</span><span class="sxs-lookup"><span data-stu-id="022c1-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="022c1-140">Récupère le nom de la langue audio avec le LCID spécifié.</span><span class="sxs-lookup"><span data-stu-id="022c1-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="022c1-141">suivant</span><span class="sxs-lookup"><span data-stu-id="022c1-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="022c1-142">Définit l’élément actuel à l’élément suivant dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="022c1-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="022c1-143">pause</span><span class="sxs-lookup"><span data-stu-id="022c1-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="022c1-144">Suspend la diffusion de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="022c1-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="022c1-145">répétition</span><span class="sxs-lookup"><span data-stu-id="022c1-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="022c1-146">Entraîne le démarrage de la diffusion de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="022c1-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="022c1-147">playItem</span><span class="sxs-lookup"><span data-stu-id="022c1-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="022c1-148">Entraîne le démarrage de la lecture de l’élément multimédia en cours ou reprend la lecture d’un élément suspendu.</span><span class="sxs-lookup"><span data-stu-id="022c1-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="022c1-149">previous</span><span class="sxs-lookup"><span data-stu-id="022c1-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="022c1-150">Définit l’élément actuel à l’élément précédent dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="022c1-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="022c1-151">première</span><span class="sxs-lookup"><span data-stu-id="022c1-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="022c1-152">Entraîne le blocage de la lecture de l’élément multimédia vidéo actuel sur le frame suivant.</span><span class="sxs-lookup"><span data-stu-id="022c1-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="022c1-153">stop</span><span class="sxs-lookup"><span data-stu-id="022c1-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="022c1-154">Arrête la diffusion de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="022c1-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="022c1-155">L’objet **Controls** est accessible par le biais de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="022c1-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="022c1-156">Object</span><span class="sxs-lookup"><span data-stu-id="022c1-156">Object</span></span>                      | <span data-ttu-id="022c1-157">Propriété</span><span class="sxs-lookup"><span data-stu-id="022c1-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="022c1-158">Lecteur</span><span class="sxs-lookup"><span data-stu-id="022c1-158">Player</span></span>](player-object.md) | [<span data-ttu-id="022c1-159">commandes</span><span class="sxs-lookup"><span data-stu-id="022c1-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="022c1-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="022c1-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022c1-161">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="022c1-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




