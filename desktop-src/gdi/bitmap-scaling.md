---
description: La fonction StretchBlt met à l’échelle un bitmap en effectuant un transfert de bloc de bits à partir d’un rectangle dans un contexte de périphérique source dans un rectangle dans un contexte de périphérique de destination.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Mise à l’échelle des bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114731"
---
# <a name="bitmap-scaling"></a><span data-ttu-id="d0063-103">Mise à l’échelle des bitmaps</span><span class="sxs-lookup"><span data-stu-id="d0063-103">Bitmap Scaling</span></span>

<span data-ttu-id="d0063-104">La fonction [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) met à l’échelle un bitmap en effectuant un transfert de bloc de bits à partir d’un rectangle dans un contexte de périphérique source dans un rectangle dans un contexte de périphérique de destination.</span><span class="sxs-lookup"><span data-stu-id="d0063-104">The [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) function scales a bitmap by performing a bit-block transfer from a rectangle in a source device context into a rectangle in a destination device context.</span></span> <span data-ttu-id="d0063-105">Toutefois, contrairement à la fonction [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , qui duplique les dimensions du rectangle source dans le rectangle de destination, **StretchBlt** permet à une application de spécifier les dimensions des rectangles source et de destination.</span><span class="sxs-lookup"><span data-stu-id="d0063-105">However, unlike the [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) function, which duplicates the source rectangle dimensions in the destination rectangle, **StretchBlt** allows an application to specify the dimensions of both the source and the destination rectangles.</span></span> <span data-ttu-id="d0063-106">Lorsque la bitmap de destination est plus petite que la bitmap source, le système combine des lignes ou des colonnes de données de couleur (ou les deux) dans le bitmap avant de restituer l’image correspondante sur le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d0063-106">When the destination bitmap is smaller than the source bitmap, the system combines rows or columns of color data (or both) in the bitmap before rendering the corresponding image on the display device.</span></span> <span data-ttu-id="d0063-107">Le système combine les données de couleur en fonction du mode Stretch spécifié, que l’application définit en appelant la fonction [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) .</span><span class="sxs-lookup"><span data-stu-id="d0063-107">The system combines the color data according to the specified stretch mode, which the application defines by calling the [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) function.</span></span> <span data-ttu-id="d0063-108">Lorsque le bitmap de destination est plus grand que la bitmap source, le système met à l’échelle ou agrandit en conséquence chaque pixel de l’image résultante.</span><span class="sxs-lookup"><span data-stu-id="d0063-108">When the destination bitmap is larger than the source bitmap, the system scales or magnifies each pixel in the resultant image accordingly.</span></span>

 

 



