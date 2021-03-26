---
description: 'Lorsque vous créez un objet Pen, vous pouvez indiquer la largeur du stylet comme l’un des arguments du constructeur. Vous pouvez également modifier la largeur du stylet à l’aide de la méthode Pen :: SetWidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Définition de la largeur et de l’alignement du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564686"
---
# <a name="setting-pen-width-and-alignment"></a><span data-ttu-id="d9bb5-104">Définition de la largeur et de l’alignement du stylet</span><span class="sxs-lookup"><span data-stu-id="d9bb5-104">Setting Pen Width and Alignment</span></span>

<span data-ttu-id="d9bb5-105">Lorsque vous créez un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , vous pouvez indiquer la largeur du stylet comme l’un des arguments du constructeur.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-105">When you create a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="d9bb5-106">Vous pouvez également modifier la largeur du stylet à l’aide de la méthode [**Pen :: SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .</span><span class="sxs-lookup"><span data-stu-id="d9bb5-106">You can also change the pen width by using the [**Pen::SetWidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) method.</span></span>

<span data-ttu-id="d9bb5-107">Une ligne théorique a une largeur de zéro.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-107">A theoretical line has a width of zero.</span></span> <span data-ttu-id="d9bb5-108">Quand vous dessinez une ligne, les pixels sont centrés sur la ligne théorique.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-108">When you draw a line, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="d9bb5-109">L’exemple suivant dessine une ligne spécifiée deux fois : une fois avec un stylet noir de largeur 1 et une fois avec un stylet vert de la largeur 10.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-109">The following example draws a specified line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



<span data-ttu-id="d9bb5-110">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-110">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="d9bb5-111">Les pixels verts et les pixels noirs sont centrés sur la ligne théorique.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-111">The green pixels and the black pixels are centered on the theoretical line.</span></span>

![<span data-ttu-id="d9bb5-112">Illustration montrant une ligne noire fine, en diagonale, entourée d’un trait vert épais</span><span class="sxs-lookup"><span data-stu-id="d9bb5-112">illustration showing a thin, diagonal, black line surrounded by a wide, green line</span></span> ](images/pens1a.png)

<span data-ttu-id="d9bb5-113">L’exemple suivant dessine un rectangle spécifié deux fois : une fois avec un stylet noir de largeur 1 et une fois avec un stylet vert de la largeur 10.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-113">The following example draws a specified rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span> <span data-ttu-id="d9bb5-114">Le code passe la valeur **PenAlignmentCenter** (un élément de l’énumération [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) à la méthode [**Pen :: SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) pour spécifier que les pixels dessinés avec le stylet vert sont centrés sur la limite du rectangle.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-114">The code passes the value **PenAlignmentCenter** (an element of the [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) enumeration) to the [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) method to specify that the pixels drawn with the green pen are centered on the boundary of the rectangle.</span></span>


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



<span data-ttu-id="d9bb5-115">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-115">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="d9bb5-116">Les pixels verts sont centrés sur le rectangle théorique, représenté par les pixels noirs.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-116">The green pixels are centered on the theoretical rectangle, which is represented by the black pixels.</span></span>

![Illustration montrant une fine ligne noire dans la forme d’un rectangle, entourée d’une ligne verte plus grande](images/pens2.png)

<span data-ttu-id="d9bb5-118">Vous pouvez modifier l’alignement du stylet vert en modifiant la troisième instruction de l’exemple précédent comme suit :</span><span class="sxs-lookup"><span data-stu-id="d9bb5-118">You can change the green pen's alignment by modifying the third statement in the preceding example as follows:</span></span>


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



<span data-ttu-id="d9bb5-119">À présent, les pixels de la ligne verte de l’épaisseur apparaissent à l’intérieur du rectangle, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-119">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration.</span></span>

![Illustration montrant une fine ligne noire dans la forme d’un rectange, englobant une ligne verte de la même forme](images/pens3.png)

 

 



