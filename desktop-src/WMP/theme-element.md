---
title: Élément THEMe
description: Élément THEMe
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Apparences du lecteur Windows Media, élément de thème
- apparences, élément THEMe
- Élément THEMe
- référence pour les apparences, élément THEMe
- éléments, thème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839645"
---
# <a name="theme-element"></a><span data-ttu-id="240b7-108">Élément THEMe</span><span class="sxs-lookup"><span data-stu-id="240b7-108">THEME Element</span></span>

<span data-ttu-id="240b7-109">L’élément **Theme** est l’élément de niveau parent d’une apparence et contient un ou plusieurs éléments **View** , qui à leur tour contiennent tous les autres éléments d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="240b7-109">The **THEME** element is the parent-level element of a skin, and contains one or more **VIEW** elements, which in turn contain all other elements within a skin.</span></span> <span data-ttu-id="240b7-110">Dans le code de script, l’élément **Theme** est accessible via l’attribut global **Theme** plutôt que via un nom spécifié par un attribut **ID** , ce qui n’est pas pris en charge par l’élément **Theme** .</span><span class="sxs-lookup"><span data-stu-id="240b7-110">Within script code, the **THEME** element is accessed through the **theme** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **THEME** element.</span></span>

<span data-ttu-id="240b7-111">L’élément **Theme** prend en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="240b7-111">The **THEME** element supports the following attributes.</span></span>



| <span data-ttu-id="240b7-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="240b7-112">Attribute</span></span>                                | <span data-ttu-id="240b7-113">Description</span><span class="sxs-lookup"><span data-stu-id="240b7-113">Description</span></span>                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="240b7-114">auteur</span><span class="sxs-lookup"><span data-stu-id="240b7-114">author</span></span>](theme-author.md)               | <span data-ttu-id="240b7-115">Spécifie ou récupère le nom de l’auteur de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="240b7-115">Specifies or retrieves the name of the author of the skin.</span></span>                                                                      |
| [<span data-ttu-id="240b7-116">authorVersion</span><span class="sxs-lookup"><span data-stu-id="240b7-116">authorVersion</span></span>](theme-authorversion.md) | <span data-ttu-id="240b7-117">Spécifie ou récupère le numéro de version de l’apparence, tel qu’il est assigné par l’auteur.</span><span class="sxs-lookup"><span data-stu-id="240b7-117">Specifies or retrieves the version number of the skin as assigned by the author.</span></span>                                                |
| [<span data-ttu-id="240b7-118">intellectuelle</span><span class="sxs-lookup"><span data-stu-id="240b7-118">copyright</span></span>](theme-copyright.md)         | <span data-ttu-id="240b7-119">Spécifie ou récupère la chaîne de copyright pour l’apparence.</span><span class="sxs-lookup"><span data-stu-id="240b7-119">Specifies or retrieves the copyright string for the skin.</span></span>                                                                       |
| [<span data-ttu-id="240b7-120">currentViewID</span><span class="sxs-lookup"><span data-stu-id="240b7-120">currentViewID</span></span>](theme-currentviewid.md) | <span data-ttu-id="240b7-121">Spécifie ou récupère la **vue** actuellement affichée.</span><span class="sxs-lookup"><span data-stu-id="240b7-121">Specifies or retrieves the currently displayed **VIEW**.</span></span>                                                                        |
| [<span data-ttu-id="240b7-122">title</span><span class="sxs-lookup"><span data-stu-id="240b7-122">title</span></span>](theme-title.md)                 | <span data-ttu-id="240b7-123">Spécifie ou récupère le titre de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="240b7-123">Specifies or retrieves the title of the skin.</span></span>                                                                                   |
| [<span data-ttu-id="240b7-124">version</span><span class="sxs-lookup"><span data-stu-id="240b7-124">version</span></span>](theme-version.md)             | <span data-ttu-id="240b7-125">Spécifie ou récupère le numéro de version du lecteur Windows Media pour lequel l’apparence a été créée.</span><span class="sxs-lookup"><span data-stu-id="240b7-125">Specifies or retrieves the Windows Media Player version number for which the skin was authored.</span></span> <span data-ttu-id="240b7-126">Ne peut être défini qu’au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="240b7-126">Can only be set at design time.</span></span> |



 

<span data-ttu-id="240b7-127">L’élément **Theme** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="240b7-127">The **THEME** element supports the following methods.</span></span>



| <span data-ttu-id="240b7-128">Méthode</span><span class="sxs-lookup"><span data-stu-id="240b7-128">Method</span></span>                                         | <span data-ttu-id="240b7-129">Description</span><span class="sxs-lookup"><span data-stu-id="240b7-129">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="240b7-130">Évènement CloseView</span><span class="sxs-lookup"><span data-stu-id="240b7-130">closeView</span></span>](theme-closeview.md)               | <span data-ttu-id="240b7-131">Ferme une **vue** ouverte.</span><span class="sxs-lookup"><span data-stu-id="240b7-131">Closes an open **VIEW**.</span></span>                                                                                        |
| [<span data-ttu-id="240b7-132">loadPreference</span><span class="sxs-lookup"><span data-stu-id="240b7-132">loadPreference</span></span>](theme-loadpreference.md)     | <span data-ttu-id="240b7-133">Charge une préférence à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="240b7-133">Loads a preference from the registry.</span></span>                                                                           |
| [<span data-ttu-id="240b7-134">logString</span><span class="sxs-lookup"><span data-stu-id="240b7-134">logString</span></span>](theme-logstring.md)               | <span data-ttu-id="240b7-135">Consigne une chaîne définie par l’utilisateur dans le fichier d’erreur si la journalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="240b7-135">Logs a user-defined string to the error file, if logging is enabled.</span></span>                                            |
| [<span data-ttu-id="240b7-136">openDialog</span><span class="sxs-lookup"><span data-stu-id="240b7-136">openDialog</span></span>](theme-opendialog.md)             | <span data-ttu-id="240b7-137">Ouvre une boîte de dialogue de fichier.</span><span class="sxs-lookup"><span data-stu-id="240b7-137">Opens a file dialog box.</span></span>                                                                                        |
| [<span data-ttu-id="240b7-138">openView</span><span class="sxs-lookup"><span data-stu-id="240b7-138">openView</span></span>](theme-openview.md)                 | <span data-ttu-id="240b7-139">Ouvre une **vue** dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="240b7-139">Opens a **VIEW** in a new window.</span></span>                                                                               |
| [<span data-ttu-id="240b7-140">openViewRelative</span><span class="sxs-lookup"><span data-stu-id="240b7-140">openViewRelative</span></span>](theme-openviewrelative.md) | <span data-ttu-id="240b7-141">Ouvre une **vue** dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="240b7-141">Opens a **VIEW** in a new window at a specified initial position relative to the upper-left corner of the skin.</span></span> |
| [<span data-ttu-id="240b7-142">playSound</span><span class="sxs-lookup"><span data-stu-id="240b7-142">playSound</span></span>](theme-playsound.md)               | <span data-ttu-id="240b7-143">Lit le fichier son spécifié.</span><span class="sxs-lookup"><span data-stu-id="240b7-143">Plays the specified sound file.</span></span>                                                                                 |
| [<span data-ttu-id="240b7-144">savePreference</span><span class="sxs-lookup"><span data-stu-id="240b7-144">savePreference</span></span>](theme-savepreference.md)     | <span data-ttu-id="240b7-145">Enregistre une préférence dans le registre.</span><span class="sxs-lookup"><span data-stu-id="240b7-145">Saves a preference in the registry.</span></span>                                                                             |
| [<span data-ttu-id="240b7-146">showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="240b7-146">showErrorDialog</span></span>](theme-showerrordialog.md)   | <span data-ttu-id="240b7-147">Affiche la boîte de dialogue erreur standard.</span><span class="sxs-lookup"><span data-stu-id="240b7-147">Displays the standard error dialog box.</span></span>                                                                         |



 

<span data-ttu-id="240b7-148">L’élément **Theme** ne prend pas en charge les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="240b7-148">The **THEME** element does not support event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="240b7-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="240b7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="240b7-150">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="240b7-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




