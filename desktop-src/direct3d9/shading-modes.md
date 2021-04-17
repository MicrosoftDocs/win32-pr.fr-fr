---
description: Le mode d’ombrage utilisé pour afficher un polygone a un effet profond sur son apparence. Les modes d’ombrage déterminent l’intensité de la couleur et de l’éclairage à n’importe quel point d’une face de polygone. Direct3D prend en charge deux modes d’ombrage.
ms.assetid: vs|directx_sdk|~\shading_modes.htm
title: Modes d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84e791bed0098838760f10f6605f716444e7688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567164"
---
# <a name="shading-modes-direct3d-9"></a>Modes d’ombrage (Direct3D 9)

Le mode d’ombrage utilisé pour afficher un polygone a un effet profond sur son apparence. Les modes d’ombrage déterminent l’intensité de la couleur et de l’éclairage à n’importe quel point d’une face de polygone. Direct3D prend en charge deux modes d’ombrage.

-   [Ombrage plat](#flat-shading)
-   [Ombrage Gouraud](#gouraud-shading)

## <a name="flat-shading"></a>Ombrage plat

Dans le mode d’ombrage plat, le pipeline de rendu Direct3D affiche un polygone, en utilisant la couleur du matériau polygonal à son premier vertex comme couleur de l’ensemble du polygone. les objets 3D qui sont rendus avec un ombrage plat ont des bords nets visibles entre les polygones s’ils ne sont pas coplanés.

L’illustration suivante montre un rendu de théière avec un ombrage plat. Le contour de chaque polygone est clairement visible. L’ombrage plat est la forme la plus rapide de l’ombrage.

![illustration d’un théière à l’aide d’un ombrage plat](images/flattea.png)

## <a name="gouraud-shading"></a>Ombrage Gouraud

Lorsque Direct3D effectue le rendu d’un polygone à l’aide de l’ombrage Gouraud, il calcule une couleur pour chaque vertex à l’aide des paramètres de normalisation et d’éclairage des vertex. Ensuite, il interpole la couleur sur la face des polygones. l’interpolation est effectuée de façon linéaire. Par exemple, si le composant rouge de la couleur du vertex 1 est 0,8 et que le composant rouge du Vertex 2 est 0,4, à l’aide du mode d’ombrage Gouraud et du modèle de couleurs RVB, le module d’éclairage Direct3D affecte un composant rouge de 0,6 au pixel situé au milieu de la ligne entre ces sommets.

L’illustration suivante montre l’ombrage Gouraud. Ce théière est composé de nombreux polygones plats et triangulaires. Toutefois, l’ombrage Gouraud rend l’affichage courbé et lisse de la surface de l’objet.

![illustration de théière à l’aide de l’ombrage Gouraud](images/gourtea.png)

L’ombrage Gouraud peut également être utilisé pour afficher des objets avec des bords tranchants.

Pour plus d’informations, consultez [vecteurs normaux de face et vertex (Direct3D 9)](face-and-vertex-normal-vectors.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ombrage](shading.md)
</dt> </dl>

 

 



