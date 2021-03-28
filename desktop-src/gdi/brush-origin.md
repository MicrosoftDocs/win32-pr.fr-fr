---
description: Quand une application appelle une fonction de dessin pour peindre une forme, le système positionne un pinceau au début de l’opération de peinture et mappe un pixel dans le pinceau bitmap à la zone cliente à l’origine de la fenêtre, qui est l’angle supérieur gauche de la fenêtre.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origine du pinceau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566568"
---
# <a name="brush-origin"></a><span data-ttu-id="30b1c-103">Origine du pinceau</span><span class="sxs-lookup"><span data-stu-id="30b1c-103">Brush Origin</span></span>

<span data-ttu-id="30b1c-104">Quand une application appelle une fonction de dessin pour peindre une forme, le système positionne un pinceau au début de l’opération de peinture et mappe un pixel dans le pinceau bitmap à la zone cliente à l’origine de la *fenêtre*, qui est l’angle supérieur gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="30b1c-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="30b1c-105">Les coordonnées du pixel que les mappages système sont appelées l' *origine du pinceau*.</span><span class="sxs-lookup"><span data-stu-id="30b1c-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="30b1c-106">L’origine du pinceau par défaut se trouve dans le coin supérieur gauche de l’image bitmap du pinceau, aux coordonnées (0,0).</span><span class="sxs-lookup"><span data-stu-id="30b1c-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="30b1c-107">Le système copie ensuite le pinceau dans la zone cliente, en formant un modèle aussi grand que l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="30b1c-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="30b1c-108">L’opération de copie continue, ligne par ligne, jusqu’à ce que la totalité de la zone cliente soit remplie.</span><span class="sxs-lookup"><span data-stu-id="30b1c-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="30b1c-109">Toutefois, le motif de pinceau est visible uniquement dans les limites de la forme spécifiée.</span><span class="sxs-lookup"><span data-stu-id="30b1c-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="30b1c-110">Il y a des instances lorsque l’origine du pinceau par défaut ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="30b1c-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="30b1c-111">Par exemple, il peut être nécessaire pour une application d’utiliser le même pinceau pour peindre les arrière-plans de ses fenêtres parent et enfant et de fusionner l’arrière-plan d’une fenêtre enfant avec celle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="30b1c-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="30b1c-112">Pour ce faire, l’application doit réinitialiser l’origine du pinceau en appelant la fonction [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) et en décalant le nombre requis de pixels de l’origine.</span><span class="sxs-lookup"><span data-stu-id="30b1c-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="30b1c-113">(Une application peut récupérer l’origine du pinceau en cours en appelant la fonction [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .)</span><span class="sxs-lookup"><span data-stu-id="30b1c-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="30b1c-114">L’illustration suivante montre une étoile à cinq branches remplie à l’aide d’un pinceau défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="30b1c-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="30b1c-115">L’illustration montre une image avec zoom du pinceau, ainsi que l’emplacement auquel elle a été mappée au début de l’opération de peinture.</span><span class="sxs-lookup"><span data-stu-id="30b1c-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![Illustration montrant que l’origine du pinceau est mappée à l’origine de la fenêtre](images/csbru-01.png)

 

 



