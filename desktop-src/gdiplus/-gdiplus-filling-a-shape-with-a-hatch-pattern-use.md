---
description: 'Un motif hachuré est constitué de deux couleurs : une pour l’arrière-plan et une pour les lignes qui forment le modèle sur l’arrière-plan.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Remplissage d’une forme avec un motif hachuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987752"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a><span data-ttu-id="13dc0-103">Remplissage d’une forme avec un motif hachuré</span><span class="sxs-lookup"><span data-stu-id="13dc0-103">Filling a Shape with a Hatch Pattern</span></span>

<span data-ttu-id="13dc0-104">Un motif hachuré est constitué de deux couleurs : une pour l’arrière-plan et une pour les lignes qui forment le modèle sur l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="13dc0-104">A hatch pattern is made from two colors: one for the background and one for the lines that form the pattern over the background.</span></span> <span data-ttu-id="13dc0-105">Pour remplir une forme fermée avec un modèle hachuré, utilisez un objet [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) .</span><span class="sxs-lookup"><span data-stu-id="13dc0-105">To fill a closed shape with a hatch pattern, use a [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) object.</span></span> <span data-ttu-id="13dc0-106">L’exemple suivant montre comment remplir une ellipse avec un modèle de hachurage :</span><span class="sxs-lookup"><span data-stu-id="13dc0-106">The following example demonstrates how to fill an ellipse with a hatch pattern:</span></span>


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



<span data-ttu-id="13dc0-107">L’illustration suivante montre l’Ellipse remplie.</span><span class="sxs-lookup"><span data-stu-id="13dc0-107">The following illustration shows the filled ellipse.</span></span>

![illustration d’une Ellipse remplie d’un motif hachuré de lignes horizontales sur un arrière-plan Uni](images/hatch1.png)

<span data-ttu-id="13dc0-109">Le constructeur [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) prend trois arguments : le style de hachurage, la couleur de la ligne hachurée et la couleur de l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="13dc0-109">The [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) constructor takes three arguments: the hatch style, the color of the hatch line, and the color of the background.</span></span> <span data-ttu-id="13dc0-110">L’argument de style de hachurage peut être n’importe quel élément de l’énumération [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) .</span><span class="sxs-lookup"><span data-stu-id="13dc0-110">The hatch style argument can be any element of the [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) enumeration.</span></span> <span data-ttu-id="13dc0-111">Il y a plus de 50 éléments dans l’énumération **HatchStyle** ; quelques-uns de ces éléments sont affichés dans la liste suivante :</span><span class="sxs-lookup"><span data-stu-id="13dc0-111">There are more than fifty elements in the **HatchStyle** enumeration; a few of those elements are shown in the following list:</span></span>

-   <span data-ttu-id="13dc0-112">**HatchStyleHorizontal**</span><span class="sxs-lookup"><span data-stu-id="13dc0-112">**HatchStyleHorizontal**</span></span>
-   <span data-ttu-id="13dc0-113">**HatchStyleVertical**</span><span class="sxs-lookup"><span data-stu-id="13dc0-113">**HatchStyleVertical**</span></span>
-   <span data-ttu-id="13dc0-114">**HatchStyleForwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="13dc0-114">**HatchStyleForwardDiagonal**</span></span>
-   <span data-ttu-id="13dc0-115">**HatchStyleBackwardDiagonal**</span><span class="sxs-lookup"><span data-stu-id="13dc0-115">**HatchStyleBackwardDiagonal**</span></span>
-   <span data-ttu-id="13dc0-116">**HatchStyleCross**</span><span class="sxs-lookup"><span data-stu-id="13dc0-116">**HatchStyleCross**</span></span>
-   <span data-ttu-id="13dc0-117">**HatchStyleDiagonalCross**</span><span class="sxs-lookup"><span data-stu-id="13dc0-117">**HatchStyleDiagonalCross**</span></span>

 

 



