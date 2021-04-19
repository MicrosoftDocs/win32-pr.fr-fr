---
title: Vue d’ensemble de l’API zoom
description: Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Agrandissement
- applications d’agrandissement d’écran
- Agrandissement
- traitement des images personnalisées
- Magnification.dll
- création de contrôles de loupe
- agrandissement sélectif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511085"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="216ea-110">Vue d’ensemble de l’API zoom</span><span class="sxs-lookup"><span data-stu-id="216ea-110">Magnification API Overview</span></span>

<span data-ttu-id="216ea-111">L’API d’agrandissement permet aux fournisseurs de technologies d’assistance de développer des applications d’agrandissement d’écran qui s’exécutent sur Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="216ea-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="216ea-112">Cette rubrique décrit l’API d’agrandissement et explique comment l’utiliser dans une application.</span><span class="sxs-lookup"><span data-stu-id="216ea-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="216ea-113">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="216ea-113">It contains the following sections:</span></span>

- [<span data-ttu-id="216ea-114">Prise en main</span><span class="sxs-lookup"><span data-stu-id="216ea-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="216ea-115">Concepts de base</span><span class="sxs-lookup"><span data-stu-id="216ea-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="216ea-116">Types de loupes</span><span class="sxs-lookup"><span data-stu-id="216ea-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="216ea-117">Facteur d’agrandissement</span><span class="sxs-lookup"><span data-stu-id="216ea-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="216ea-118">Effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="216ea-119">Rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="216ea-120">Liste de filtres</span><span class="sxs-lookup"><span data-stu-id="216ea-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="216ea-121">Transformation d’entrée</span><span class="sxs-lookup"><span data-stu-id="216ea-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="216ea-122">Curseur système</span><span class="sxs-lookup"><span data-stu-id="216ea-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="216ea-123">Initialisation de la bibliothèque Runtime de la loupe</span><span class="sxs-lookup"><span data-stu-id="216ea-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="216ea-124">Utilisation de la loupe Full-Screen</span><span class="sxs-lookup"><span data-stu-id="216ea-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="216ea-125">Utilisation du contrôle magnifier</span><span class="sxs-lookup"><span data-stu-id="216ea-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="216ea-126">Création du contrôle magnifier</span><span class="sxs-lookup"><span data-stu-id="216ea-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="216ea-127">Initialisation du contrôle</span><span class="sxs-lookup"><span data-stu-id="216ea-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="216ea-128">Définition du rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="216ea-129">Application d’effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="216ea-130">Agrandissement sélectif</span><span class="sxs-lookup"><span data-stu-id="216ea-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="216ea-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="216ea-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="216ea-132">Mise en route</span><span class="sxs-lookup"><span data-stu-id="216ea-132">Getting Started</span></span>

<span data-ttu-id="216ea-133">La version d’origine de l’API d’agrandissement est prise en charge sur les systèmes d’exploitation Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="216ea-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="216ea-134">Sur Windows 8 et versions ultérieures, l’API prend en charge des fonctionnalités supplémentaires, notamment l’agrandissement plein écran et la définition de la visibilité du curseur système agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="216ea-135">La prise en charge de l’API d’agrandissement est fournie par Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="216ea-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="216ea-136">Pour compiler votre application, incluez grossissement. h et un lien vers grossissement. lib.</span><span class="sxs-lookup"><span data-stu-id="216ea-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="216ea-137">L’API d’agrandissement n’est pas prise en charge sous WOW64 ; autrement dit, une application de loupe 32 bits ne s’exécutera pas correctement sous Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="216ea-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="216ea-138">Concepts de base</span><span class="sxs-lookup"><span data-stu-id="216ea-138">Basic Concepts</span></span>

<span data-ttu-id="216ea-139">Cette section décrit les concepts fondamentaux sur lesquels l’API d’agrandissement est basée.</span><span class="sxs-lookup"><span data-stu-id="216ea-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="216ea-140">Il contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="216ea-140">It contains the following parts:</span></span>

- [<span data-ttu-id="216ea-141">Types de loupes</span><span class="sxs-lookup"><span data-stu-id="216ea-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="216ea-142">Facteur d’agrandissement</span><span class="sxs-lookup"><span data-stu-id="216ea-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="216ea-143">Effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="216ea-144">Rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="216ea-145">Liste de filtres</span><span class="sxs-lookup"><span data-stu-id="216ea-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="216ea-146">Transformation d’entrée</span><span class="sxs-lookup"><span data-stu-id="216ea-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="216ea-147">Curseur système</span><span class="sxs-lookup"><span data-stu-id="216ea-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="216ea-148">Types de loupes</span><span class="sxs-lookup"><span data-stu-id="216ea-148">Types of Magnifiers</span></span>

<span data-ttu-id="216ea-149">L’API prend en charge deux types d’agrandisseurs : la *loupe plein écran* et le *contrôle magnifier*.</span><span class="sxs-lookup"><span data-stu-id="216ea-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="216ea-150">La loupe plein écran agrandit le contenu de l’écran tout entier, tandis que le contrôle magnifier agrandit le contenu d’une zone particulière de l’écran et affiche le contenu dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="216ea-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="216ea-151">Pour les deux loupes, les images et le texte sont agrandis, et tous deux vous permettent de contrôler la quantité d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="216ea-152">Vous pouvez également appliquer des effets de couleur au contenu de l’écran agrandi, ce qui vous permet de voir plus facilement les personnes qui ont des défauts de couleurs ou des couleurs qui ont un contraste plus ou moins élevé.</span><span class="sxs-lookup"><span data-stu-id="216ea-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="216ea-153">L’API de contrôle magnifier est disponible sur les systèmes d’exploitation Windows Vista et versions ultérieures, tandis que l’API magnifier plein écran est disponible uniquement sur les systèmes d’exploitation Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="216ea-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="216ea-154">Facteur d’agrandissement</span><span class="sxs-lookup"><span data-stu-id="216ea-154">Magnification Factor</span></span>

<span data-ttu-id="216ea-155">La loupe plein écran et le contrôle magnifier appliquent une transformation d’échelle pour agrandir le contenu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="216ea-156">La quantité de grossissement appliquée par la transformation d’échelle est appelée *facteur d’agrandissement*.</span><span class="sxs-lookup"><span data-stu-id="216ea-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="216ea-157">Elle est exprimée sous la forme d’une valeur à virgule flottante où 1,0 correspond à aucun grossissement, tandis que les valeurs supérieures produisent une quantité d’agrandissement correspondante.</span><span class="sxs-lookup"><span data-stu-id="216ea-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="216ea-158">Par exemple, la valeur 1,5 rend le contenu de l’écran de 50% plus grand.</span><span class="sxs-lookup"><span data-stu-id="216ea-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="216ea-159">Un facteur d’agrandissement inférieur à 1,0 n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="216ea-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="216ea-160">Effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-160">Color Effects</span></span>

<span data-ttu-id="216ea-161">Les effets de couleur sont obtenus en appliquant une matrice de transformation de couleur 5 par 5 aux couleurs du contenu de l’écran agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="216ea-162">La matrice détermine les intensités des composants rouge, bleu, vert et alpha du contenu.</span><span class="sxs-lookup"><span data-stu-id="216ea-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="216ea-163">Pour plus d’informations, consultez [utilisation d’une matrice de couleurs pour transformer une couleur unique](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) dans la documentation de Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="216ea-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="216ea-164">Rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-164">Source Rectangle</span></span>

<span data-ttu-id="216ea-165">La loupe plein écran applique la transformation de mise à l’échelle et la transformation de couleur à l’écran entier.</span><span class="sxs-lookup"><span data-stu-id="216ea-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="216ea-166">En revanche, le contrôle magnifier copie une zone de l’écran, appelée *rectangle source*, vers une image bitmap hors écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="216ea-167">Ensuite, le contrôle applique la transformation d’échelle et la transformation de couleur, le cas échéant, à la bitmap hors écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="216ea-168">Enfin, le contrôle affiche le bitmap mis à l’échelle et transformé en couleurs dans la fenêtre de contrôle de la loupe.</span><span class="sxs-lookup"><span data-stu-id="216ea-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="216ea-169">Liste de filtres</span><span class="sxs-lookup"><span data-stu-id="216ea-169">Filter List</span></span>

<span data-ttu-id="216ea-170">Par défaut, le contrôle magnifier agrandit toutes les fenêtres du rectangle source spécifié.</span><span class="sxs-lookup"><span data-stu-id="216ea-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="216ea-171">Toutefois, en fournissant une *liste de filtres* de handles de fenêtre, vous pouvez contrôler les fenêtres qui sont incluses dans le contenu agrandi et celles qui ne le sont pas.</span><span class="sxs-lookup"><span data-stu-id="216ea-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="216ea-172">Pour plus d’informations, consultez [grossissement sélectif](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="216ea-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="216ea-173">La loupe plein écran ne prend pas en charge une liste de filtres ; elle agrandit toujours toutes les fenêtres à l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="216ea-174">Transformation d’entrée</span><span class="sxs-lookup"><span data-stu-id="216ea-174">Input Transform</span></span>

<span data-ttu-id="216ea-175">Normalement, le contenu de l’écran agrandi est « invisible » au stylet ou à l’entrée tactile de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="216ea-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="216ea-176">Par exemple, si l’utilisateur appuie sur l’image agrandie d’un contrôle, le système ne passe pas nécessairement l’entrée au contrôle.</span><span class="sxs-lookup"><span data-stu-id="216ea-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="216ea-177">Au lieu de cela, le système passe l’entrée à n’importe quel élément (le cas échéant) sur les coordonnées d’écran taraudé sur le Bureau non agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="216ea-178">La fonction [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) vous permet de spécifier une *transformation d’entrée* qui mappe l’espace de coordonnées du contenu de l’écran agrandi à l’espace de coordonnées d’écran réel (non agrandi).</span><span class="sxs-lookup"><span data-stu-id="216ea-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="216ea-179">Cela permet au système de passer une entrée de stylet ou de toucher entrée dans le contenu d’écran agrandi, à l’élément d’interface utilisateur approprié à l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="216ea-180">Le processus appelant doit disposer de privilèges UIAccess pour définir la transformation d’entrée.</span><span class="sxs-lookup"><span data-stu-id="216ea-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="216ea-181">Pour plus d’informations, consultez Considérations sur la [sécurité d’UI Automation](../uiauto-securityoverview.md) et [/MANIFESTUAC (incorpore les informations de contrôle de compte d’utilisateur dans le manifeste)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span><span class="sxs-lookup"><span data-stu-id="216ea-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="216ea-182">Curseur système</span><span class="sxs-lookup"><span data-stu-id="216ea-182">System Cursor</span></span>

<span data-ttu-id="216ea-183">La fonction [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) vous permet d’afficher ou de masquer le curseur système.</span><span class="sxs-lookup"><span data-stu-id="216ea-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="216ea-184">Si vous affichez le curseur système lorsque la loupe plein écran est active, le curseur système est toujours agrandi avec le reste du contenu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="216ea-185">Si vous masquez le curseur système lorsque la loupe plein écran est active, le curseur système n’est pas visible du tout.</span><span class="sxs-lookup"><span data-stu-id="216ea-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="216ea-186">Avec le contrôle Magnifier, la fonction [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) affiche ou masque le curseur système non agrandi, mais n’a aucun effet sur le curseur système agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="216ea-187">La visibilité du curseur système agrandi varie selon que le contrôle magnifier a le style [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="216ea-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="216ea-188">S’il a ce style, le contrôle magnifier affiche le curseur système agrandi, ainsi que le contenu de l’écran agrandi, chaque fois que le curseur système entre dans le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="216ea-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="216ea-189">Initialisation de la bibliothèque Runtime de la loupe</span><span class="sxs-lookup"><span data-stu-id="216ea-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="216ea-190">Avant de pouvoir appeler d’autres fonctions de l’API loupe, vous devez créer et initialiser les objets d’exécution de la loupe en appelant la fonction [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) .</span><span class="sxs-lookup"><span data-stu-id="216ea-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="216ea-191">De même, une fois que vous avez fini d’utiliser l’API Magnifier, appelez la fonction [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) pour détruire les objets d’exécution de la loupe et libérer les ressources système associées.</span><span class="sxs-lookup"><span data-stu-id="216ea-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="216ea-192">Utilisation de la loupe Full-Screen</span><span class="sxs-lookup"><span data-stu-id="216ea-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="216ea-193">Pour utiliser la loupe plein écran, appelez la fonction [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="216ea-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="216ea-194">Le paramètre *magLevel* spécifie le facteur d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="216ea-195">Les paramètres *xoffset* et *yOffset* spécifient la façon dont le contenu de l’écran agrandi est positionné par rapport à l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="216ea-196">Lorsque le contenu de l’écran est agrandi, il devient plus grand que l’écran lui-même.</span><span class="sxs-lookup"><span data-stu-id="216ea-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="216ea-197">Une partie du contenu s’étend au-delà des bords de l’écran et devient invisible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="216ea-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="216ea-198">Les paramètres *xoffset* et *yOffset* de la fonction [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) déterminent la partie du contenu de l’écran agrandie qui s’affiche à l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="216ea-199">Ensemble, les paramètres spécifient les coordonnées d’un point dans le contenu de l’écran qui n’est pas agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="216ea-200">Lorsque le contenu est agrandi, il est positionné avec le point spécifié dans l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="216ea-201">L’exemple suivant définit le facteur d’agrandissement de la loupe plein écran et place le centre du contenu de l’écran agrandi au centre de l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="216ea-202">Utilisez la fonction [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) pour appliquer des effets de couleur au contenu plein écran en définissant une matrice de transformation des couleurs définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="216ea-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="216ea-203">Par exemple, l’exemple suivant définit une matrice de transformation des couleurs qui convertit les couleurs en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="216ea-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="216ea-204">Vous pouvez récupérer le facteur d’agrandissement et les valeurs de décalage actuels en appelant la fonction [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) .</span><span class="sxs-lookup"><span data-stu-id="216ea-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="216ea-205">Vous pouvez récupérer la matrice de transformation de couleur actuelle en appelant la fonction [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) .</span><span class="sxs-lookup"><span data-stu-id="216ea-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="216ea-206">Utilisation du contrôle magnifier</span><span class="sxs-lookup"><span data-stu-id="216ea-206">Using the Magnifier Control</span></span>

<span data-ttu-id="216ea-207">Le contrôle magnifier agrandit le contenu d’une zone particulière de l’écran et affiche le contenu dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="216ea-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="216ea-208">Cette section décrit comment utiliser le contrôle magnifier.</span><span class="sxs-lookup"><span data-stu-id="216ea-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="216ea-209">Il contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="216ea-209">It contains the following parts:</span></span>

- [<span data-ttu-id="216ea-210">Création du contrôle magnifier</span><span class="sxs-lookup"><span data-stu-id="216ea-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="216ea-211">Initialisation du contrôle</span><span class="sxs-lookup"><span data-stu-id="216ea-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="216ea-212">Définition du rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="216ea-213">Application d’effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="216ea-214">Agrandissement sélectif</span><span class="sxs-lookup"><span data-stu-id="216ea-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="216ea-215">Création du contrôle magnifier</span><span class="sxs-lookup"><span data-stu-id="216ea-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="216ea-216">Le contrôle magnifier doit être hébergé dans une fenêtre créée avec le style étendu [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="216ea-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="216ea-217">Après avoir créé la fenêtre hôte, appelez [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) pour définir l’opacité de la fenêtre hôte.</span><span class="sxs-lookup"><span data-stu-id="216ea-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="216ea-218">La fenêtre hôte est généralement définie sur l’opacité totale pour empêcher le contenu de l’écran sous-jacent de s’affiche.</span><span class="sxs-lookup"><span data-stu-id="216ea-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="216ea-219">L’exemple suivant montre comment définir l’opacité complète de la fenêtre hôte :</span><span class="sxs-lookup"><span data-stu-id="216ea-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="216ea-220">Si vous appliquez le style de [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) à la fenêtre hôte, les clics de souris sont passés à l’objet situé derrière la fenêtre hôte à l’emplacement du curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="216ea-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="216ea-221">Sachez que, étant donné que la fenêtre hôte ne traite pas les clics de souris, l’utilisateur ne peut pas déplacer ou redimensionner la fenêtre d’agrandissement à l’aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="216ea-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="216ea-222">La classe de fenêtre de la fenêtre de contrôle loupe doit être **WC_MAGNIFIER**.</span><span class="sxs-lookup"><span data-stu-id="216ea-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="216ea-223">Si vous appliquez le style de [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) , le contrôle loupe comprend le curseur système dans le contenu de l’écran agrandi et le curseur est agrandi avec le contenu de l’écran.</span><span class="sxs-lookup"><span data-stu-id="216ea-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="216ea-224">Après avoir créé le contrôle Magnifier, conservez le handle de fenêtre pour pouvoir le passer à d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="216ea-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="216ea-225">L’exemple suivant montre comment créer le contrôle magnifier.</span><span class="sxs-lookup"><span data-stu-id="216ea-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="216ea-226">Initialisation du contrôle</span><span class="sxs-lookup"><span data-stu-id="216ea-226">Initializing the Control</span></span>

<span data-ttu-id="216ea-227">Après avoir créé le contrôle Magnifier, vous devez appeler la fonction [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) pour spécifier le facteur d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="216ea-228">Il suffit de spécifier une matrice de</span><span class="sxs-lookup"><span data-stu-id="216ea-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="216ea-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="216ea-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="216ea-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="216ea-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="216ea-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="216ea-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="216ea-232">où *n* est le facteur d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="216ea-233">L’exemple suivant montre comment définir le facteur d’agrandissement du contrôle magnifier.</span><span class="sxs-lookup"><span data-stu-id="216ea-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="216ea-234">Définition du rectangle source</span><span class="sxs-lookup"><span data-stu-id="216ea-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="216ea-235">Lorsque l’utilisateur déplace le curseur de la souris autour de l’écran, votre application appelle la fonction [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) pour spécifier la partie de l’écran sous-jacent qui doit être agrandie.</span><span class="sxs-lookup"><span data-stu-id="216ea-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="216ea-236">L’exemple de fonction suivant calcule la position et les dimensions du rectangle source (en fonction de la position de la souris et des dimensions de la fenêtre de la loupe divisée par le facteur d’agrandissement) et définit le rectangle source en conséquence.</span><span class="sxs-lookup"><span data-stu-id="216ea-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="216ea-237">La fonction Centre également la zone cliente de la fenêtre hôte à la position de la souris.</span><span class="sxs-lookup"><span data-stu-id="216ea-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="216ea-238">Cette fonction est appelée à des intervalles pour mettre à jour la fenêtre d’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="216ea-239">Application d’effets de couleur</span><span class="sxs-lookup"><span data-stu-id="216ea-239">Applying Color Effects</span></span>

<span data-ttu-id="216ea-240">Un contrôle magnifier qui a le style [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) applique une matrice de transformation de couleur intégrée qui inverse les couleurs du contenu de l’écran agrandi.</span><span class="sxs-lookup"><span data-stu-id="216ea-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="216ea-241">L’illustration suivante montre le contenu de l’écran dans un contrôle magnifier qui a le style **MS_INVERTCOLORS** .</span><span class="sxs-lookup"><span data-stu-id="216ea-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![capture d’écran du contenu agrandi avec les couleurs inversées](images/color-inversion.png)

<span data-ttu-id="216ea-243">La fonction [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) vous permet d’appliquer d’autres effets de couleur en définissant une matrice de transformation des couleurs définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="216ea-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="216ea-244">Par exemple, la fonction suivante définit une matrice de transformation des couleurs qui convertit les couleurs en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="216ea-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="216ea-245">Pour plus d’informations sur le fonctionnement des transformations de couleurs, consultez [utilisation d’une matrice de couleurs pour transformer une couleur unique](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) dans la documentation GDI+.</span><span class="sxs-lookup"><span data-stu-id="216ea-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="216ea-246">Agrandissement sélectif</span><span class="sxs-lookup"><span data-stu-id="216ea-246">Selective Magnification</span></span>

<span data-ttu-id="216ea-247">Par défaut, l’agrandissement est appliqué à toutes les fenêtres autres que la fenêtre d’agrandissement elle-même.</span><span class="sxs-lookup"><span data-stu-id="216ea-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="216ea-248">Pour spécifier les fenêtres à agrandir, appelez la fonction [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) .</span><span class="sxs-lookup"><span data-stu-id="216ea-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="216ea-249">Cette méthode prend une liste de fenêtres à agrandir ou une liste de fenêtres à exclure de l’agrandissement.</span><span class="sxs-lookup"><span data-stu-id="216ea-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="216ea-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="216ea-250">Related topics</span></span>

[<span data-ttu-id="216ea-251">API de grossissement</span><span class="sxs-lookup"><span data-stu-id="216ea-251">Magnification API</span></span>](entry-magapi-sdk.md)