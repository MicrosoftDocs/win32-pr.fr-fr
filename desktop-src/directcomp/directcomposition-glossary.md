---
title: Glossaire DirectComposition
description: Cette rubrique définit les termes de Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315564"
---
# <a name="directcomposition-glossary"></a><span data-ttu-id="e4934-103">Glossaire DirectComposition</span><span class="sxs-lookup"><span data-stu-id="e4934-103">DirectComposition glossary</span></span>

> [!NOTE]
> <span data-ttu-id="e4934-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e4934-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="e4934-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="e4934-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="e4934-106">Cette rubrique définit les termes de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="e4934-106">This topic defines Microsoft DirectComposition terms.</span></span>

<dl> <dt>

<span data-ttu-id="e4934-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**fonction d’animation**</span><span class="sxs-lookup"><span data-stu-id="e4934-107"><span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animation function**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-108">Construction qui spécifie comment la valeur d’une propriété d’objet unique change sur une période donnée.</span><span class="sxs-lookup"><span data-stu-id="e4934-108">A construct that specifies how the value of a single object property changes over a period of time.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objet d’animation**</span><span class="sxs-lookup"><span data-stu-id="e4934-109"><span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**animation object**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-110">Objet qui représente une fonction permettant d’animer les propriétés d’un autre objet.</span><span class="sxs-lookup"><span data-stu-id="e4934-110">An object that represents a function for animating the properties of another object.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segment d’animation**</span><span class="sxs-lookup"><span data-stu-id="e4934-111"><span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**animation segment**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-112">Définitions de minuterie fondamentales d’une fonction d’animation ; Il s’agit des primitives à partir desquelles les fonctions d’animation plus complexes et de niveau supérieur sont générées.</span><span class="sxs-lookup"><span data-stu-id="e4934-112">The fundamental timing definitions of an animation function; they are the primitives from which more complex and higher level animation functions are built.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**mémoire tampon d’arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="e4934-113"><span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**back buffer**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-114">Rectangle de mémoire dans lequel une application peut écrire directement.</span><span class="sxs-lookup"><span data-stu-id="e4934-114">A rectangle of memory that an application can directly write to.</span></span> <span data-ttu-id="e4934-115">La mémoire tampon d’arrière-plan n’est jamais directement affichée sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="e4934-115">The back buffer is never directly displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**feuilles**</span><span class="sxs-lookup"><span data-stu-id="e4934-116"><span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-117">Groupe d’appels de méthode DirectComposition traités atomiquement.</span><span class="sxs-lookup"><span data-stu-id="e4934-117">A group of DirectComposition method calls that are processed atomically.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**pixels**</span><span class="sxs-lookup"><span data-stu-id="e4934-118"><span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-119">Mémoire tampon de couleur, avec ou sans canal alpha, qui réside dans la mémoire système ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="e4934-119">A color buffer, either with or without an alpha channel, that resides in system or video memory.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**mode bordure**</span><span class="sxs-lookup"><span data-stu-id="e4934-120"><span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**border mode**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-121">Propriété d’un visuel Microsoft DirectComposition qui affecte la façon dont les bords d’une bitmap sont composés lorsque la bitmap est transformée, de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées entières.</span><span class="sxs-lookup"><span data-stu-id="e4934-121">A property of a Microsoft DirectComposition visual that affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not axis-aligned with integer coordinates.</span></span> <span data-ttu-id="e4934-122">Cela affecte également la façon dont le contenu est coupé aux angles d’un élément qui a des angles arrondis, et au bord d’un élément qui est transformé de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées d’entier.</span><span class="sxs-lookup"><span data-stu-id="e4934-122">It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not axis-aligned with integer coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip, objet**</span><span class="sxs-lookup"><span data-stu-id="e4934-123"><span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip object**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-124">Objet qui représente un rectangle de découpage.</span><span class="sxs-lookup"><span data-stu-id="e4934-124">A object that represents a clip rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**Rectangle de découpage**</span><span class="sxs-lookup"><span data-stu-id="e4934-125"><span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**clip rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-126">Ensemble de coordonnées qui définissent la zone du contenu de la bitmap du visuel qui est dessinée sur l’écran lorsque la bitmap est restituée.</span><span class="sxs-lookup"><span data-stu-id="e4934-126">A set of coordinates that define the area of visual's bitmap content that is drawn on the screen when the bitmap is rendered.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**masquer**</span><span class="sxs-lookup"><span data-stu-id="e4934-127"><span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**cloak**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-128">Pour empêcher temporairement Gestionnaire de fenêtrage (DWM) de dessiner une fenêtre à l’écran.</span><span class="sxs-lookup"><span data-stu-id="e4934-128">To temporarily prevent Desktop Window Manager (DWM) from drawing a window to the display.</span></span> <span data-ttu-id="e4934-129">En général, les applications masquent une fenêtre lorsque DirectComposition utilise l’image bitmap de la fenêtre dans une composition.</span><span class="sxs-lookup"><span data-stu-id="e4934-129">Applications typically cloak a window while DirectComposition uses the window's bitmap in a composition.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**valider**</span><span class="sxs-lookup"><span data-stu-id="e4934-130"><span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-131">Pour soumettre un lot de commandes à DirectCompositionDirectComposition pour traitement.</span><span class="sxs-lookup"><span data-stu-id="e4934-131">To submit a batch of commands to DirectCompositionDirectComposition for processing.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**mode composite**</span><span class="sxs-lookup"><span data-stu-id="e4934-132"><span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**composite mode**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-133">L’une des différentes façons de fusionner deux bitmaps (source et destination) pour obtenir un effet particulier.</span><span class="sxs-lookup"><span data-stu-id="e4934-133">One of several ways of blending two bitmaps (a source and a destination) to achieve a particular effect.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span><span class="sxs-lookup"><span data-stu-id="e4934-134"><span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-135">Collection de bitmaps qui sont combinés et manipulés en appliquant diverses transformations, effets et animations pour produire un résultat visuel prévu dans une interface utilisateur d’application.</span><span class="sxs-lookup"><span data-stu-id="e4934-135">A collection of bitmaps that are combined and manipulated by applying various transforms, effects, and animations to produce an intended visual result in an application UI.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**fenêtre cible de la composition**</span><span class="sxs-lookup"><span data-stu-id="e4934-136"><span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**composition target window**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-137">Fenêtre à laquelle une arborescence d’éléments visuels est liée et dans laquelle la composition obtenue est dessinée.</span><span class="sxs-lookup"><span data-stu-id="e4934-137">The window to which a visual tree is bound, and in which the resulting composition is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**résultat**</span><span class="sxs-lookup"><span data-stu-id="e4934-138"><span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effect**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-139">Opération qui modifie la manière dont les bitmaps d’une arborescence d’éléments visuels sont pixellisées, en général en appliquant un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="e4934-139">An operation that modifies how the bitmaps of a visual tree are rasterized, typically by applying a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Groupe d’effets**</span><span class="sxs-lookup"><span data-stu-id="e4934-140"><span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**effect group**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-141">Groupe d’effets bitmap appliqués ensemble pour modifier la pixellisation d’une sous-arborescence d’un visuel.</span><span class="sxs-lookup"><span data-stu-id="e4934-141">A group of bitmap effects that are applied together to modify the rasterization of a visual’s sub-tree.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**Frame**</span><span class="sxs-lookup"><span data-stu-id="e4934-142"><span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-143">Itération du moteur de composition qui produit une pixellisation de l’arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="e4934-143">An iteration of the composition engine that produces a rasterization of the visual tree.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**mémoire tampon d’avant**</span><span class="sxs-lookup"><span data-stu-id="e4934-144"><span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**front buffer**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-145">Rectangle de mémoire qui est traduit par la carte graphique et affiché sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="e4934-145">A rectangle of memory that is translated by the graphics adapter and displayed on the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**mode d’interpolation**</span><span class="sxs-lookup"><span data-stu-id="e4934-146"><span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**interpolation mode**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-147">Propriété qui détermine la façon dont une bitmap est composée lorsqu’elle est transformée de telle sorte qu’il n’y a pas de correspondance un-à-un entre les pixels de la bitmap et les pixels de l’écran.</span><span class="sxs-lookup"><span data-stu-id="e4934-147">A property that determines how a bitmap is composed when it is transformed such that there is no one-to-one correspondence between pixels in the bitmap and pixels on the screen.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**visuel racine**</span><span class="sxs-lookup"><span data-stu-id="e4934-148"><span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**root visual**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-149">Visuel à partir duquel tous les autres éléments visuels dans une arborescence d’éléments visuels sont décroissants.</span><span class="sxs-lookup"><span data-stu-id="e4934-149">The visual from which all other visuals in a visual tree are descended.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**chaîne de permutation**</span><span class="sxs-lookup"><span data-stu-id="e4934-150"><span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-151">Collection d’une ou plusieurs mémoires tampons d’arrière-plan qui peuvent être présentées en série au tampon d’avant.</span><span class="sxs-lookup"><span data-stu-id="e4934-151">A collection of one or more back buffers that can be serially presented to the front buffer</span></span>

</dd> <dt>

<span data-ttu-id="e4934-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surfaces**</span><span class="sxs-lookup"><span data-stu-id="e4934-152"><span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surface**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-153">Représentation d’une zone linéaire de la mémoire d’affichage qui réside généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="e4934-153">A representation of a linear area of display memory that usually resides in the display memory of the display card, although surfaces can exist in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Modifiez**</span><span class="sxs-lookup"><span data-stu-id="e4934-154"><span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-155">Matrice qui représente une transformation de coordonnée dans un espace à deux dimensions ou trois dimensions.</span><span class="sxs-lookup"><span data-stu-id="e4934-155">A matrix that represents a coordinate transformation in either two-dimensional or three-dimensional space.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Groupe transformer**</span><span class="sxs-lookup"><span data-stu-id="e4934-156"><span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**transform group**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-157">Collection de transformations dont les matrices sont multipliées dans l’ordre dans lequel elles sont spécifiées dans la collection avant qu’elles ne soient appliquées à un visuel.</span><span class="sxs-lookup"><span data-stu-id="e4934-157">A collection of transforms whose matrices are multiplied together in the order in which they are specified in the collection before they are applied to a visual.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**</span><span class="sxs-lookup"><span data-stu-id="e4934-158"><span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**visual**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-159">Objet qui contient une référence facultative à un objet bitmap et un ensemble de propriétés qui déterminent où et comment la bitmap est restituée à l’écran.</span><span class="sxs-lookup"><span data-stu-id="e4934-159">An object that contains an optional reference to a bitmap object, and a set of properties that determine where and how the bitmap is rendered to the screen.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objet visuel**</span><span class="sxs-lookup"><span data-stu-id="e4934-160"><span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**visual object**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-161">Consultez [*visuel*](/windows).</span><span class="sxs-lookup"><span data-stu-id="e4934-161">See [*visual*](/windows).</span></span>

</dd> <dt>

<span data-ttu-id="e4934-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**sous-arborescence visuelle**</span><span class="sxs-lookup"><span data-stu-id="e4934-162"><span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**visual subtree**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-163">Partie d’une arborescence d’éléments visuels composée d’un visuel particulier et de tous ses éléments visuels enfants et descendants.</span><span class="sxs-lookup"><span data-stu-id="e4934-163">A portion of a visual tree consisting of a particular visual and all of its child and descendent visuals.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**arborescence d’éléments visuels**</span><span class="sxs-lookup"><span data-stu-id="e4934-164"><span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**visual tree**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-165">Collection hiérarchique d’éléments visuels utilisés pour créer une composition.</span><span class="sxs-lookup"><span data-stu-id="e4934-165">A hierarchical collection of visuals used to create a composition.</span></span>

</dd> <dt>

<span data-ttu-id="e4934-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**chaîne de permutation sans fenêtre**</span><span class="sxs-lookup"><span data-stu-id="e4934-166"><span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**windowless swap chain**</span></span>
</dt> <dd>

<span data-ttu-id="e4934-167">Chaîne de permutation associée à un objet visuel DirectComposition à la place d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e4934-167">A swap chain that is associated with a DirectComposition visual object instead of a window.</span></span>

</dd> </dl>

 

 