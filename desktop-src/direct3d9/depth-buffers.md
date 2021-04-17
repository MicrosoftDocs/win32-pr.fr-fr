---
description: Une mémoire tampon de profondeur, souvent appelée « z-buffer » ou « w-buffer », est une propriété de l’appareil qui stocke les informations de profondeur à utiliser par Direct3D.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Mémoires tampons de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481552"
---
# <a name="depth-buffers-direct3d-9"></a>Mémoires tampons de profondeur (Direct3D 9)

Une mémoire tampon de profondeur, souvent appelée « z-buffer » ou « w-buffer », est une propriété de l’appareil qui stocke les informations de profondeur à utiliser par Direct3D. Lorsque Direct3D effectue le rendu d’une scène sur une surface cible, il peut utiliser la mémoire d’une surface de mémoire tampon de profondeur associée en tant qu’espace de travail pour déterminer la façon dont les pixels de polygones sont occultait l’un l’autre. Direct3D utilise une surface Direct3D hors écran comme cible dans laquelle les valeurs de couleur finales sont écrites. La surface de mémoire tampon de profondeur associée à la surface de la cible de rendu est utilisée pour stocker les informations de profondeur qui indiquent à Direct3D la profondeur de chaque pixel visible dans la scène.

Quand une scène est pixellisée avec la mise en mémoire tampon de profondeur activée, chaque point sur la surface de rendu est testé. Les valeurs de la mémoire tampon de profondeur peuvent être la coordonnée z d’un point ou sa coordonnée w homogène-à partir de l’emplacement (x, y, z, w) du point dans l’espace de projection. Une mémoire tampon de profondeur qui utilise des valeurs z est souvent appelée une mémoire tampon z, et une autre qui utilise des valeurs w est appelée une mémoire tampon w. Chaque type de mémoire tampon de profondeur présente des avantages et des inconvénients, qui sont décrits plus loin.

Au début du test, la valeur de profondeur dans le tampon de profondeur est définie sur la plus grande valeur possible pour la scène. La valeur de couleur sur la surface de rendu est définie sur la valeur de couleur d’arrière-plan ou sur la valeur de couleur de la texture d’arrière-plan à ce stade. Chaque polygone de la scène est testé pour voir s’il croise les coordonnées actuelles (x, y) sur la surface de rendu. Si c’est le cas, la valeur de profondeur, qui est la coordonnée z dans une mémoire tampon z, et la coordonnée w dans une mémoire tampon w-au point actuel sont testées pour voir s’il est plus petit que la valeur de profondeur stockée dans le tampon de profondeur. Si la profondeur de la valeur de polygone est plus petite, elle est stockée dans le tampon de profondeur et la valeur de couleur du polygone est écrite sur le point actuel sur la surface de rendu. Si la valeur de profondeur du polygone à ce point est supérieure, le polygone suivant de la liste est testé. Ce processus est illustré dans le diagramme suivant.

![diagramme des valeurs de profondeur de test](images/zbuffer.png)

> [!Note]  
> Bien que la plupart des applications n’utilisent pas cette fonctionnalité, vous pouvez modifier la comparaison utilisée par Direct3D pour déterminer quelles valeurs sont placées dans la mémoire tampon de profondeur et par la suite, la surface de rendu cible. Pour ce faire, modifiez la valeur de l' \_ État de rendu D3DRS ZFUNC. Sur un matériel, la modification de la fonction de comparaison peut désactiver le test z hiérarchique.

 

Presque tous les accélérateurs sur le marché prennent en charge la mise en mémoire tampon z, ce qui fait de z-buffer le type de mémoire tampon de profondeur le plus courant aujourd’hui. Néanmoins omniprésent, les tampons z présentent des inconvénients. En raison des mathématiques impliquées, les valeurs z générées dans une mémoire tampon z ont tendance à ne pas être distribuées uniformément dans la plage de la mémoire tampon z (en général 0,0 à 1,0, inclusivement). Plus précisément, le ratio entre les plans de découpage FAR et near affecte fortement la manière dont les valeurs z sont distribuées de manière inégale. À l’aide d’une distance plane jusqu’au taux de distance à proximité du plan de 100, 90% de la plage de mémoire tampon de profondeur est consacrée aux 10 premiers% de la plage de profondeur de la scène. Les applications typiques pour le divertissement ou les simulations visuelles avec des scènes extérieures nécessitent souvent des ratios plan/proche du plan de n’importe où entre 1 000 et 10 000. À un ratio de 1 000, 98% de la plage est passé sur les 2 premiers% de la plage de profondeur, et la distribution se complique avec des ratios plus élevés. Cela peut entraîner des artefacts de surface masqués dans les objets distants, en particulier lors de l’utilisation de mémoires tampons de profondeur 16 bits, la profondeur de bit la plus souvent prise en charge.

Une mémoire tampon de profondeur basée sur w, en revanche, est souvent plus uniformément répartie entre les plans de clip near et Far qu’une mémoire tampon z. L’avantage clé est que le rapport entre les distances des plans de découpage FAR et near n’est plus un problème. Cela permet aux applications de prendre en charge des plages maximales de grande taille, tout en continuant d’obtenir une mise en mémoire tampon de profondeur relativement précise jusqu’au point oculaire. Une mémoire tampon de profondeur basée sur w n’est pas parfaite et peut parfois présenter des artefacts de surface masqués pour des objets proches. L’une des inconvénients de l’approche w-buffer est liée à la prise en charge matérielle : la mise en mémoire tampon w n’est pas prise en charge aussi largement que la mise en mémoire tampon z dans le matériel.

L’utilisation d’une mémoire tampon z requiert une surcharge lors du rendu. Diverses techniques peuvent être utilisées pour optimiser le rendu lors de l’utilisation de la mise en mémoire tampon z. Pour plus d’informations, consultez [Z-buffer performance](performance-optimizations.md).

> [!Note]  
> L’interprétation réelle d’une valeur de profondeur est spécifique au convertisseur.

 

Cette section présente des informations sur l’utilisation des tampons de profondeur pour la ligne masquée et la suppression de la surface masquée.

-   [Interrogation de la prise en charge des tampons de profondeur (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Création d’un tampon de profondeur (Direct3D 9)](creating-a-depth-buffer.md)
-   [Activation de la mise en mémoire tampon de profondeur (Direct3D 9)](enabling-depth-buffering.md)
-   [Récupération d’une mémoire tampon de profondeur (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Effacement des tampons de profondeur (Direct3D 9)](clearing-depth-buffers.md)
-   [Modification de l’accès en écriture au tampon de profondeur (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Modification des fonctions de comparaison du tampon de profondeur (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu Direct3D](direct3d-rendering.md)
</dt> </dl>

 

 



