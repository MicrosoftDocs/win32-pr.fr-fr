---
description: Vous pouvez dessiner le début ou la fin d’une ligne dans l’une des différentes formes appelées lignes d’épaisseur de ligne. Windows GDI+ prend en charge plusieurs extrémités de ligne, telles que l’arrondi, le carré, le losange et la flèche.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Dessin d’une ligne avec des embouts de ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988306"
---
# <a name="drawing-a-line-with-line-caps"></a><span data-ttu-id="d4e76-104">Dessin d’une ligne avec des embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="d4e76-104">Drawing a Line with Line Caps</span></span>

<span data-ttu-id="d4e76-105">Vous pouvez dessiner le début ou la fin d’une ligne dans l’une des différentes formes appelées lignes d’épaisseur de ligne.</span><span class="sxs-lookup"><span data-stu-id="d4e76-105">You can draw the start or end of a line in one of several shapes called line caps.</span></span> <span data-ttu-id="d4e76-106">Windows GDI+ prend en charge plusieurs extrémités de ligne, telles que l’arrondi, le carré, le losange et la flèche.</span><span class="sxs-lookup"><span data-stu-id="d4e76-106">Windows GDI+ supports several line caps, such as round, square, diamond, and arrowhead.</span></span>

<span data-ttu-id="d4e76-107">Vous pouvez spécifier des extrémités de ligne pour le début d’une ligne (extrémité de début), la fin d’une ligne (extrémité de fin) ou les tirets d’une ligne en pointillés (tirets).</span><span class="sxs-lookup"><span data-stu-id="d4e76-107">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>

<span data-ttu-id="d4e76-108">L’exemple suivant dessine une ligne avec une flèche à une extrémité et une extrémité arrondie à l’autre extrémité :</span><span class="sxs-lookup"><span data-stu-id="d4e76-108">The following example draws a line with an arrowhead at one end and a round cap at the other end:</span></span>


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



<span data-ttu-id="d4e76-109">L’illustration suivante montre la ligne résultante.</span><span class="sxs-lookup"><span data-stu-id="d4e76-109">The following illustration shows the resulting line.</span></span>

![Illustration montrant une ligne horizontale avec une flèche à l’extrémité gauche et un cercle à l’extrémité droite](images/pens4.png)

<span data-ttu-id="d4e76-111">**LineCapArrowAnchor** et **LineCapRoundAnchor** sont des éléments de l’énumération [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .</span><span class="sxs-lookup"><span data-stu-id="d4e76-111">**LineCapArrowAnchor** and **LineCapRoundAnchor** are elements of the [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) enumeration.</span></span>

 

 



