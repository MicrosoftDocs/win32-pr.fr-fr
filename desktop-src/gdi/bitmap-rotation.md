---
description: Pour copier une image bitmap dans un parallélogramme ; Utilisez la fonction PlgBlt, qui effectue un transfert de bloc de bits à partir d’un rectangle dans un contexte de périphérique source dans un parallélogramme dans un contexte de périphérique de destination.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Rotation de bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991284"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="8eb9e-103">Rotation de bitmap</span><span class="sxs-lookup"><span data-stu-id="8eb9e-103">Bitmap Rotation</span></span>

<span data-ttu-id="8eb9e-104">Pour copier une image bitmap dans un parallélogramme ; Utilisez la fonction [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , qui effectue un transfert de bloc de bits à partir d’un rectangle dans un contexte de périphérique source dans un parallélogramme dans un contexte de périphérique de destination.</span><span class="sxs-lookup"><span data-stu-id="8eb9e-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="8eb9e-105">Pour faire pivoter la bitmap, une application doit fournir les coordonnées, en unités universelles, à utiliser pour les angles du parallélogramme.</span><span class="sxs-lookup"><span data-stu-id="8eb9e-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="8eb9e-106">(Pour plus d’informations sur la rotation et les unités universelles, consultez [espaces de coordonnées et transformations](coordinate-spaces-and-transformations.md).)</span><span class="sxs-lookup"><span data-stu-id="8eb9e-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



