---
title: Élément VIEW
description: Élément VIEW
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Apparences du lecteur Windows Media, élément d’affichage
- Skins, élément VIEW
- Élément VIEW
- informations de référence sur les apparences, l’élément VIEW
- éléments, vue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380068"
---
# <a name="view-element"></a><span data-ttu-id="14130-108">Élément VIEW</span><span class="sxs-lookup"><span data-stu-id="14130-108">VIEW Element</span></span>

<span data-ttu-id="14130-109">L’élément **View** contient les détails de l’interface utilisateur d’une apparence et utilise les attributs, les méthodes et les gestionnaires d’événements présentés dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="14130-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="14130-110">Plusieurs éléments de **vue** peuvent être définis en tant qu’enfants de l’élément **Theme** d’une apparence pour fournir différentes interfaces pour différentes situations.</span><span class="sxs-lookup"><span data-stu-id="14130-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="14130-111">Les éléments d' **affichage** ne peuvent pas être spécifiés en tant qu’enfants de tout autre élément et ils contiennent tous les autres éléments d’apparence.</span><span class="sxs-lookup"><span data-stu-id="14130-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="14130-112">Notez que chaque vue a sa propre portée variable, ce qui signifie qu’elle ne peut pas partager des valeurs d’attribut avec d’autres vues.</span><span class="sxs-lookup"><span data-stu-id="14130-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="14130-113">L’attribut global **View** peut être utilisé pour référencer un élément **View** spécifique à partir de n’importe où dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="14130-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="14130-114">Il s’agit d’une alternative à l’utilisation de son attribut **ID** , qui doit être utilisé à partir d’autres éléments d' **affichage** ou à partir de l’élément de **thème** .</span><span class="sxs-lookup"><span data-stu-id="14130-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="14130-115">L’élément **View** prend en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="14130-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="14130-116">Les attributs marqués d’un astérisque ( \* ) sont également pris en charge par l’élément **subview** .</span><span class="sxs-lookup"><span data-stu-id="14130-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="14130-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="14130-117">Attribute</span></span>                                                       | <span data-ttu-id="14130-118">Description</span><span class="sxs-lookup"><span data-stu-id="14130-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14130-119">[backgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="14130-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="14130-120">Spécifie ou récupère la couleur d’arrière-plan de la **vue** ou de la sous- **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="14130-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="14130-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="14130-122">Spécifie ou récupère l’image d’arrière-plan de la **vue** ou de la sous- **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="14130-123">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="14130-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="14130-124">Spécifie ou récupère la valeur de décalage de la teinte de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="14130-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="14130-125">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="14130-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="14130-126">Spécifie ou récupère la valeur de saturation de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="14130-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="14130-127">[backgroundTiled](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="14130-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="14130-128">Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan de la **vue** ou de la sous- **vue** est affichée en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="14130-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="14130-129">category</span><span class="sxs-lookup"><span data-stu-id="14130-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="14130-130">Spécifie ou récupère la catégorie pour laquelle l’interface utilisateur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="14130-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="14130-131">focusObjectID</span><span class="sxs-lookup"><span data-stu-id="14130-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="14130-132">Spécifie ou récupère une valeur indiquant l’élément qui a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="14130-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="14130-133">Telle</span><span class="sxs-lookup"><span data-stu-id="14130-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="14130-134">Spécifie ou récupère la hauteur maximale de la **vue** lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="14130-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="14130-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="14130-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="14130-136">Spécifie ou récupère la largeur maximale de la **vue** lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="14130-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="14130-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="14130-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="14130-138">Spécifie ou récupère la hauteur minimale de la **vue** lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="14130-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="14130-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="14130-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="14130-140">Spécifie ou récupère la largeur minimale de la **vue** lors du redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="14130-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="14130-141">redimensionnable</span><span class="sxs-lookup"><span data-stu-id="14130-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="14130-142">Spécifie ou récupère une valeur indiquant si la **vue** peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="14130-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="14130-143">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="14130-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="14130-144">Spécifie ou récupère une valeur indiquant si l’image d’arrière-plan peut être redimensionnée.</span><span class="sxs-lookup"><span data-stu-id="14130-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="14130-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="14130-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="14130-146">Spécifie les noms de fichiers des fichiers JScript associés.</span><span class="sxs-lookup"><span data-stu-id="14130-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="14130-147">timerInterval</span><span class="sxs-lookup"><span data-stu-id="14130-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="14130-148">Spécifie ou récupère l’intervalle, en millisecondes, auquel la minuterie déclenche des événements dans le gestionnaire d’événements **OnTimer** .</span><span class="sxs-lookup"><span data-stu-id="14130-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="14130-149">title</span><span class="sxs-lookup"><span data-stu-id="14130-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="14130-150">Spécifie ou récupère le titre de la **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="14130-151">Ne peut être défini qu’au moment de la conception.</span><span class="sxs-lookup"><span data-stu-id="14130-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="14130-152">Spreadsheet</span><span class="sxs-lookup"><span data-stu-id="14130-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="14130-153">Spécifie ou récupère une valeur indiquant si la barre de titre de la fenêtre est affichée.</span><span class="sxs-lookup"><span data-stu-id="14130-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="14130-154">[transparencyColor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="14130-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="14130-155">Spécifie ou récupère la couleur de transparence de l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="14130-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="14130-156">L’élément **View** prend en charge les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="14130-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="14130-157">Méthode</span><span class="sxs-lookup"><span data-stu-id="14130-157">Method</span></span>                                              | <span data-ttu-id="14130-158">Description</span><span class="sxs-lookup"><span data-stu-id="14130-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="14130-159">close</span><span class="sxs-lookup"><span data-stu-id="14130-159">close</span></span>](view-close.md)                             | <span data-ttu-id="14130-160">Ferme la **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="14130-161">valoris</span><span class="sxs-lookup"><span data-stu-id="14130-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="14130-162">Agrandit la **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="14130-163">icône</span><span class="sxs-lookup"><span data-stu-id="14130-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="14130-164">Réduit la **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="14130-165">restore</span><span class="sxs-lookup"><span data-stu-id="14130-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="14130-166">Restaure la **vue**.</span><span class="sxs-lookup"><span data-stu-id="14130-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="14130-167">returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="14130-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="14130-168">Retourne l’utilisateur au mode complet du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="14130-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="14130-169">size</span><span class="sxs-lookup"><span data-stu-id="14130-169">size</span></span>](view-size.md)                               | <span data-ttu-id="14130-170">Redimensionne la **vue** sur un bord spécifié.</span><span class="sxs-lookup"><span data-stu-id="14130-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="14130-171">L’élément **View** peut implémenter les gestionnaires d’événements suivants.</span><span class="sxs-lookup"><span data-stu-id="14130-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="14130-172">Gestionnaire d'événements</span><span class="sxs-lookup"><span data-stu-id="14130-172">Event handler</span></span>               | <span data-ttu-id="14130-173">Description</span><span class="sxs-lookup"><span data-stu-id="14130-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="14130-174">OnClose</span><span class="sxs-lookup"><span data-stu-id="14130-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="14130-175">Gère un événement qui se produit lorsque la **vue** est sur le point d’être fermée.</span><span class="sxs-lookup"><span data-stu-id="14130-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="14130-176">OnError</span><span class="sxs-lookup"><span data-stu-id="14130-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="14130-177">Gère un événement d’erreur si **Settings. enableErrorDialogs** est défini sur false.</span><span class="sxs-lookup"><span data-stu-id="14130-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="14130-178">OnLoad</span><span class="sxs-lookup"><span data-stu-id="14130-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="14130-179">Gère un événement qui se produit lorsque la **vue** est affichée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="14130-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="14130-180">minute</span><span class="sxs-lookup"><span data-stu-id="14130-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="14130-181">Gère les événements de minuterie.</span><span class="sxs-lookup"><span data-stu-id="14130-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="14130-182">L’élément **View** prend en charge les attributs ambiants et peut implémenter les gestionnaires d’événements ambiants, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="14130-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="14130-183">Pour plus d’informations, consultez [attributs ambiants](ambient-attributes.md) et [gestionnaires d’événements ambiants](ambient-event-handlers.md),</span><span class="sxs-lookup"><span data-stu-id="14130-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="14130-184">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14130-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14130-185">**Référence de programmation de l’apparence**</span><span class="sxs-lookup"><span data-stu-id="14130-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




