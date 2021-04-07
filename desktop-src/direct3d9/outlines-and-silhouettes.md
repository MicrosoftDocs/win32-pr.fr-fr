---
description: Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Plans et silhouettes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745533"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="c4939-103">Plans et silhouettes (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c4939-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="c4939-104">Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.</span><span class="sxs-lookup"><span data-stu-id="c4939-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="c4939-105">Si votre application applique un masque de stencil à l’image d’une primitive qui est de la même forme mais légèrement inférieure, l’image résultante contient uniquement le contour de la primitive.</span><span class="sxs-lookup"><span data-stu-id="c4939-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="c4939-106">L’application peut ensuite remplir la zone masquée du gabarit de l’image avec une couleur unie, ce qui donne à la primitive un aspect en relief.</span><span class="sxs-lookup"><span data-stu-id="c4939-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="c4939-107">Si la taille et la forme du masque du gabarit sont identiques à celles de la primitive que vous affichez, l’image résultante contient un trou où la primitive doit être.</span><span class="sxs-lookup"><span data-stu-id="c4939-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="c4939-108">Votre application peut alors remplir le trou avec du noir pour produire une silhouette de la primitive.</span><span class="sxs-lookup"><span data-stu-id="c4939-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4939-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4939-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4939-110">Techniques de tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="c4939-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



