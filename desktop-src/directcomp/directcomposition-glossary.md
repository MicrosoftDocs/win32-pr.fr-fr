---
title: Glossaire DirectComposition
description: Cette rubrique définit les termes de Microsoft DirectComposition.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d6a6f39de62339bf5de0ea7b4976fa19f60c4bd2ff549a732acee43d546256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985429"
---
# <a name="directcomposition-glossary"></a>Glossaire DirectComposition

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique définit les termes de Microsoft DirectComposition.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**fonction d’animation**
</dt> <dd>

Construction qui spécifie comment la valeur d’une propriété d’objet unique change sur une période donnée.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**objet d’animation**
</dt> <dd>

Objet qui représente une fonction permettant d’animer les propriétés d’un autre objet.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segment d’animation**
</dt> <dd>

Définitions de minuterie fondamentales d’une fonction d’animation ; Il s’agit des primitives à partir desquelles les fonctions d’animation plus complexes et de niveau supérieur sont générées.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**mémoire tampon d’arrière-plan**
</dt> <dd>

Rectangle de mémoire dans lequel une application peut écrire directement. La mémoire tampon d’arrière-plan n’est jamais directement affichée sur le moniteur.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**feuilles**
</dt> <dd>

Groupe d’appels de méthode DirectComposition traités atomiquement.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**pixels**
</dt> <dd>

Mémoire tampon de couleur, avec ou sans canal alpha, qui réside dans la mémoire système ou vidéo.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**mode bordure**
</dt> <dd>

Propriété d’un visuel Microsoft DirectComposition qui affecte la façon dont les bords d’une bitmap sont composés lorsque la bitmap est transformée, de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées entières. Cela affecte également la façon dont le contenu est coupé aux angles d’un élément qui a des angles arrondis, et au bord d’un élément qui est transformé de telle sorte que les bords ne sont pas alignés sur l’axe avec les coordonnées d’entier.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip, objet**
</dt> <dd>

Objet qui représente un rectangle de découpage.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**Rectangle de découpage**
</dt> <dd>

Ensemble de coordonnées qui définissent la zone du contenu de la bitmap du visuel qui est dessinée sur l’écran lorsque la bitmap est restituée.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**masquer**
</dt> <dd>

Pour empêcher temporairement Gestionnaire de fenêtrage (DWM) de dessiner une fenêtre à l’écran. En général, les applications masquent une fenêtre lorsque DirectComposition utilise l’image bitmap de la fenêtre dans une composition.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**valider**
</dt> <dd>

Pour soumettre un lot de commandes à DirectCompositionDirectComposition pour traitement.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**mode composite**
</dt> <dd>

L’une des différentes façons de fusionner deux bitmaps (source et destination) pour obtenir un effet particulier.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**composition**
</dt> <dd>

Collection de bitmaps qui sont combinés et manipulés en appliquant diverses transformations, effets et animations pour produire un résultat visuel prévu dans une interface utilisateur d’application.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**fenêtre cible de la composition**
</dt> <dd>

Fenêtre à laquelle une arborescence d’éléments visuels est liée et dans laquelle la composition obtenue est dessinée.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**résultat**
</dt> <dd>

Opération qui modifie la manière dont les bitmaps d’une arborescence d’éléments visuels sont pixellisées, en général en appliquant un nuanceur de pixels.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**Groupe d’effets**
</dt> <dd>

Groupe d’effets bitmap appliqués ensemble pour modifier la pixellisation d’une sous-arborescence d’un visuel.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**Frame**
</dt> <dd>

Itération du moteur de composition qui produit une pixellisation de l’arborescence d’éléments visuels.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**mémoire tampon d’avant**
</dt> <dd>

Rectangle de mémoire qui est traduit par la carte graphique et affiché sur le moniteur.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**mode d’interpolation**
</dt> <dd>

Propriété qui détermine la façon dont une bitmap est composée lorsqu’elle est transformée de telle sorte qu’il n’y a pas de correspondance un-à-un entre les pixels de la bitmap et les pixels de l’écran.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**visuel racine**
</dt> <dd>

Visuel à partir duquel tous les autres éléments visuels dans une arborescence d’éléments visuels sont décroissants.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**chaîne de permutation**
</dt> <dd>

Collection d’une ou plusieurs mémoires tampons d’arrière-plan qui peuvent être présentées en série au tampon d’avant.

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**surfaces**
</dt> <dd>

Représentation d’une zone linéaire de la mémoire d’affichage qui réside généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**Modifiez**
</dt> <dd>

Matrice qui représente une transformation de coordonnée dans un espace à deux dimensions ou trois dimensions.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**Groupe transformer**
</dt> <dd>

Collection de transformations dont les matrices sont multipliées dans l’ordre dans lequel elles sont spécifiées dans la collection avant qu’elles ne soient appliquées à un visuel.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**
</dt> <dd>

Objet qui contient une référence facultative à un objet bitmap et un ensemble de propriétés qui déterminent où et comment la bitmap est restituée à l’écran.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**objet visuel**
</dt> <dd>

Consultez [*visuel*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**sous-arborescence visuelle**
</dt> <dd>

Partie d’une arborescence d’éléments visuels composée d’un visuel particulier et de tous ses éléments visuels enfants et descendants.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**arborescence d’éléments visuels**
</dt> <dd>

Collection hiérarchique d’éléments visuels utilisés pour créer une composition.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**chaîne de permutation sans fenêtre**
</dt> <dd>

Chaîne de permutation associée à un objet visuel DirectComposition à la place d’une fenêtre.

</dd> </dl>

 

 