---
description: Tout au long de la programmation Direct3D et de la fenêtre, les objets à l’écran sont référencés en termes de rectangles englobants.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rectangles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108458"
---
# <a name="rectangles-direct3d-9"></a>Rectangles (Direct3D 9)

Tout au long de la programmation Direct3D et de la fenêtre, les objets à l’écran sont référencés en termes de rectangles englobants. Les côtés d’un rectangle englobant sont toujours parallèles aux côtés de l’écran. le rectangle peut donc être décrit par deux points, l’angle supérieur gauche et le coin inférieur droit. La plupart des applications utilisent la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour transporter des informations sur un rectangle englobant à utiliser lors de la blitting à l’écran ou de l’exécution de la détection d’atteinte.

En C++, la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) a la définition suivante.


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



Dans l’exemple précédent, les membres gauche et supérieur sont les coordonnées x et y du coin supérieur gauche d’un rectangle englobant. De même, les membres droits et inférieurs composent les coordonnées du coin inférieur droit. L’illustration suivante montre comment vous pouvez visualiser ces valeurs.

![illustration du rectangle délimité par les valeurs gauche, haut, droite et inférieure](images/rect.png)

La colonne de pixels sur le bord droit et la ligne de pixels du bord inférieur ne sont pas incluses dans le RECT. Par exemple, le verrouillage d’un RECT avec les membres {10, 10, 138, 138} produit un objet 128 pixels en largeur et en hauteur.

Dans un souci d’efficacité, de cohérence et de simplicité d’utilisation, toutes les fonctions de présentation Direct3D fonctionnent avec des rectangles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Systèmes de coordonnées et géométrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
