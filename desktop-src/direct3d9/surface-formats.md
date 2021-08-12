---
description: Dans Direct3D, toutes les images à deux dimensions (2D) sont représentées par une plage linéaire de mémoire appelée surface.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Formats de surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e54b6bf4573243e170f089a72d7d5c69e31c81a536703d764694d43f2dc33cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291496"
---
# <a name="surface-formats-direct3d-9"></a>Formats de surface (Direct3D 9)

Dans Direct3D, toutes les images à deux dimensions (2D) sont représentées par une plage linéaire de mémoire appelée surface. Une surface peut être considérée comme un tableau 2D où chaque élément contient une valeur de couleur représentant une petite section de l’image, appelée pixel. Le niveau de détail d’une image est défini à la fois par le nombre de pixels nécessaires pour représenter l’image et par le nombre de bits nécessaires pour le spectre des couleurs de l’image. Par exemple, une image de 800 pixels de large par 600 pixels de haut avec 32 bits de couleur pour chaque pixel (écrit comme 800x600x32) sera plus détaillée qu’une image de 640 pixels de large par 480 pixels de hauteur avec 16 bits de couleur pour chaque pixel (écrit comme 640x480x16). De même, l’image plus détaillée nécessitera une surface plus importante pour stocker les données. Pour une image 800x600x32, les dimensions du tableau de la surface seront de 800x600, et chaque élément contiendra une valeur 32 bits pour représenter sa couleur.

Toutes les surfaces ont une taille et stockent un nombre spécifique de bits représentant la couleur. Les bits qui représentent la couleur sont séparés en éléments de couleur individuels : rouge, vert et bleu. Dans Direct3D, tous les éléments de couleur sont définis par le type énuméré [D3DFORMAT](d3dformat.md) . Un format de couleur Direct3D est divisé en nombre d’octets réservés pour chaque couleur. Par exemple, un format de couleur de 16 bits dans Direct3D est défini en tant que D3DFMT \_ R5G6B5, où 5 bits sont réservés pour le rouge (R), 6 bits pour le vert (G) et 5 bits pour le bleu (B).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 



