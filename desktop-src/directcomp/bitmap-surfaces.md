---
title: Objets bitmap
description: Cette rubrique décrit les types de contenu de bitmap que DirectComposition prend en charge.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc36253511c060b264039f27975c694272c1c916ad0067c1955fd02f00553d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089049"
---
# <a name="bitmap-objects"></a>Objets bitmap

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition est un moteur de composition d’images bitmap. Elle permet aux développeurs d’applications de combiner plusieurs bitmaps et de les manipuler de différentes façons pour obtenir des effets visuels et des animations intéressants dans une interface utilisateur d’application. Cette rubrique décrit les types de contenu de bitmap que DirectComposition prend en charge.

-   [Contenu de la bitmap](#bitmap-content)
    -   [Bitmaps de mémoire vidéo](#video-memory-bitmaps)
    -   [Bitmaps de fenêtre](#window-bitmaps)
    -   [Association d’un contenu bitmap à un visuel](#associating-bitmap-content-with-a-visual)
    -   [Canal alpha](#alpha-channel)
-   [Rubriques connexes](#related-topics)

## <a name="bitmap-content"></a>Contenu de la bitmap

Les applications fournissent à DirectComposition le contenu de la bitmap à composer et à animer en créant des objets visuels, puis en définissant la [propriété de contenu](basic-concepts.md) de ces objets. DirectComposition n’offre aucun service de pixellisation. Une application doit utiliser d’autres bibliothèques logicielles ou de pixellisation avec accélération matérielle, telles que [Direct2D](../direct2d/direct2d-portal.md) ou [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) , pour remplir les bitmaps à composer. Après la composition, DirectComposition passe le contenu de la bitmap composée à [Gestionnaire de fenêtrage (DWM)](/windows/desktop/dwm/dwm-overview) pour le rendu à l’écran.

**Types de contenu de bitmap pris en charge** Microsoft DirectComposition prend en charge les types de bitmaps suivants :

-   [Bitmaps de mémoire vidéo](#video-memory-bitmaps)
-   [Bitmaps de fenêtre](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Bitmaps de mémoire vidéo

Une image bitmap de mémoire vidéo est pixellisée dans le matériel à l’aide des méthodes Microsoft DirectX (y compris le modèle d’interopérabilité DX vers GDI). Il est associé à des surfaces partagées interprocessus qui sont visibles par l’application appelante et à DirectComposition. Une image bitmap de mémoire vidéo n’est pas sujette à rupture car l’application ne peut lire que les surfaces à partir desquelles DirectComposition les textures.

### <a name="video-content"></a>Contenu vidéo

Les applications peuvent utiliser DirectComposition pour composer des images vidéo qui utilisent des chaînes de permutation sans fenêtre DirectX qui sont liées à une surface DirectComposition. D’un point de vue conceptuel, DirectComposition traite le contenu vidéo comme une séquence de bitmaps. DirectComposition ne permet pas de présenter des images vidéo.

DirectComposition prend en charge les chaînes d’échange sans fenêtre DirectX, c’est-à-dire les chaînes de permutation qui ne sont pas liées à une fenêtre particulière, et permet à deux applications différentes de partager des chaînes d’échange sans fenêtre à travers les limites du processus. Le partage de chaînes d’échange sans fenêtre permet aux scénarios vidéo où la chaîne de permutation est créée dans un processus et est utilisée avec DirectComposition dans un deuxième processus. Les chaînes d’échange sans fenêtre sont créées à l’aide de la méthode [**IDXGIFactory2 :: CreateSwapChainForCompositionSurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

Pour plus d’informations sur les chaînes de permutation DirectX, consultez [vue d’ensemble de dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Contenu stéréo

D’un point de vue conceptuel, une chaîne de permutation stéréo se compose de surfaces d’infrastructure Microsoft DirectX Graphics (DXGI) qui représentent les canaux gauche et droit du contenu stéréo 3D. Lorsqu’une chaîne de permutation stéréo est utilisée comme ressource bitmap pour un visuel, DirectComposition compose en stéréo. Tout le contenu non stéréo (contenu mono) est considéré comme ayant le même contenu de canal de gauche et de droite. autrement dit, le même contenu de bitmap est utilisé pour les deux canaux. DirectComposition compose tout le contenu de gauche et tout le contenu approprié séparément. Si le périphérique d’affichage ne prend pas en charge la stéréo, DirectComposition traite le canal stéréo gauche ou droit (en fonction de l’application) en tant que contenu mono et compose à l’aide de ces données uniquement pour la ressource bitmap.

DirectComposition ne prend pas en charge la création ou la manipulation de contenu stéréo et ne peut pas promouvoir une chaîne de permutation mono vers une paire stéréo. Une application doit effectuer ces tâches avant de présenter le contenu stéréo DirectX à DirectComposition. En outre, une application doit fournir les décalages de canal droit et gauche pour la perception de profondeur ; DirectComposition ne peut pas ajuster les décalages de canaux gauche et droit pour modifier la profondeur perçue du contenu stéréo DirectX.

Le contenu stéréo DirectX est composé et conservé dans le DWM quand un matériel à capacité stéréo est disponible.

### <a name="window-bitmaps"></a>Bitmaps de fenêtre

Une « image bitmap Windows » n’est pas une image bitmap réelle, mais est un espace réservé que DirectComposition remplace en temps réel par des pixellisations de fenêtres enfants ou de niveau supérieur. Une image bitmap de fenêtre est semblable à une miniature DWM, à ceci près qu’une miniature peut contenir des contributions de nombreuses fenêtres, telles que des fenêtres non enfants détenues, alors qu’une image bitmap de fenêtre DirectComposition est toujours une représentation d’une seule fenêtre et de ses enfants.

Étant donné que DirectComposition a accès aux surfaces de redirection de toutes les fenêtres et à toutes les arborescences d’éléments visuels, il peut réutiliser le contenu d’une fenêtre dans plusieurs arborescences visuelles. La fenêtre doit être superposée, car une fenêtre non superposée n’a pas de surface de redirection dédiée et, par conséquent, sa pixellisation n’est pas toujours disponible pour DirectComposition.

Pour utiliser une image bitmap de fenêtre, une application associe un visuel à un handle de fenêtre (HWND). Ensuite, DirectComposition re-compose le visuel chaque fois que le contenu de la fenêtre change, y compris lorsque le contenu change suite à des modifications apportées aux arborescences d’éléments visuels associées à la fenêtre. En d’autres termes, comme les miniatures DWM, les bitmaps de fenêtre DirectComposition sont « dynamiques ».

### <a name="associating-bitmap-content-with-a-visual"></a>Association d’un contenu bitmap à un visuel

Pour les trois types de bitmaps, une application peut associer la même bitmap à plusieurs visuels, ce qui signifie qu’une allocation de mémoire unique peut être utilisée pour afficher le même contenu plusieurs fois.

### <a name="alpha-channel"></a>Canal alpha

Toutes les bitmaps ont un format 32 bits par pixel (BPP), qui comprend huit bits pour la transparence par pixel. Toutefois, une application peut spécifier la manière dont DirectComposition doit utiliser le canal alpha. En particulier, DirectComposition peut respecter le canal alpha, ou il peut ignorer l’ensemble d’alpha, auquel cas la bitmap est considérée comme étant entièrement opaque.

Un mode Alpha supplémentaire ignore le canal alpha, mais traite les valeurs rouge, vert et bleu comme des valeurs alpha par canal au lieu de l’interprétation normale de ces canaux comme des intensités de couleur. Ce mode est utile pour le rendu ClearType, qui nécessite des informations de couverture de sous-pixel. pour utiliser le mode alpha par canal, une application doit d’abord utiliser [Direct2D](../direct2d/direct2d-portal.md) et [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) pour écrire des données de couverture sous-pixel dans une image bitmap. Ensuite, l’application doit définir le mode Alpha correct et spécifier une couleur de texte lorsqu’elle associe l’image bitmap à un visuel. DirectComposition fusionne la couleur du texte avec les données de couverture, ce qui produit une fusion ClearType sur l’arrière-plan.

Dans les situations où l’algorithme ClearType n’est pas applicable, par exemple si l’image bitmap n’est pas alignée sur les pixels et alignée sur l’axe, ou si elle doit être dessinée sur une surface intermédiaire, DirectComposition peut utiliser les données de couverture de sous-pixel dans le bitmap pour produire une pixellisation en nuances de gris à la place, automatiquement et sans coût supplémentaire.

Pour plus d’informations, consultez la description du paramètre *alphaMode* de la fonction [**IDCompositionDevice :: CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) ou [**IDCompositionDevice :: CreateVirtualSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 