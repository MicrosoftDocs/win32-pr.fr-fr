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
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="36db7-103">Rectangles (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="36db7-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="36db7-104">Tout au long de la programmation Direct3D et de la fenêtre, les objets à l’écran sont référencés en termes de rectangles englobants.</span><span class="sxs-lookup"><span data-stu-id="36db7-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="36db7-105">Les côtés d’un rectangle englobant sont toujours parallèles aux côtés de l’écran. le rectangle peut donc être décrit par deux points, l’angle supérieur gauche et le coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="36db7-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="36db7-106">La plupart des applications utilisent la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) pour transporter des informations sur un rectangle englobant à utiliser lors de la blitting à l’écran ou de l’exécution de la détection d’atteinte.</span><span class="sxs-lookup"><span data-stu-id="36db7-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="36db7-107">En C++, la structure [**Rect**](/previous-versions//dd162897(v=vs.85)) a la définition suivante.</span><span class="sxs-lookup"><span data-stu-id="36db7-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="36db7-108">Dans l’exemple précédent, les membres gauche et supérieur sont les coordonnées x et y du coin supérieur gauche d’un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="36db7-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="36db7-109">De même, les membres droits et inférieurs composent les coordonnées du coin inférieur droit.</span><span class="sxs-lookup"><span data-stu-id="36db7-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="36db7-110">L’illustration suivante montre comment vous pouvez visualiser ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="36db7-110">The following illustration shows how you can visualize these values.</span></span>

![illustration du rectangle délimité par les valeurs gauche, haut, droite et inférieure](images/rect.png)

<span data-ttu-id="36db7-112">La colonne de pixels sur le bord droit et la ligne de pixels du bord inférieur ne sont pas incluses dans le RECT.</span><span class="sxs-lookup"><span data-stu-id="36db7-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="36db7-113">Par exemple, le verrouillage d’un RECT avec les membres {10, 10, 138, 138} produit un objet 128 pixels en largeur et en hauteur.</span><span class="sxs-lookup"><span data-stu-id="36db7-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="36db7-114">Dans un souci d’efficacité, de cohérence et de simplicité d’utilisation, toutes les fonctions de présentation Direct3D fonctionnent avec des rectangles.</span><span class="sxs-lookup"><span data-stu-id="36db7-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36db7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36db7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36db7-116">Systèmes de coordonnées et géométrie</span><span class="sxs-lookup"><span data-stu-id="36db7-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
