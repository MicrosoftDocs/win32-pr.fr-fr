---
description: Windows GDI+ fournit plusieurs styles de tirets qui sont répertoriés dans l’énumération DashStyle. Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tiret personnalisé.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Dessin d’une ligne en pointillés personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988025"
---
# <a name="drawing-a-custom-dashed-line"></a><span data-ttu-id="f90a9-104">Dessin d’une ligne en pointillés personnalisée</span><span class="sxs-lookup"><span data-stu-id="f90a9-104">Drawing a Custom Dashed Line</span></span>

<span data-ttu-id="f90a9-105">Windows GDI+ fournit plusieurs styles de tirets qui sont répertoriés dans l’énumération [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) .</span><span class="sxs-lookup"><span data-stu-id="f90a9-105">Windows GDI+ provides several dash styles that are listed in the [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) enumeration.</span></span> <span data-ttu-id="f90a9-106">Si ces styles de tiret standard ne répondent pas à vos besoins, vous pouvez créer un modèle de tiret personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f90a9-106">If those standard dash styles don't suit your needs, you can create a custom dash pattern.</span></span>

<span data-ttu-id="f90a9-107">Pour dessiner une ligne en pointillés personnalisée, placez les longueurs des tirets et des espaces dans un tableau et transmettez l’adresse du tableau en tant qu’argument à la méthode [**Pen :: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) d’un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="f90a9-107">To draw a custom dashed line, put the lengths of the dashes and spaces in an array and pass the address of the array as an argument to the [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) method of a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="f90a9-108">L’exemple suivant dessine une ligne en pointillés personnalisée basée sur le tableau {5, 2, 15, 4}.</span><span class="sxs-lookup"><span data-stu-id="f90a9-108">The following example draws a custom dashed line based on the array {5, 2, 15, 4}.</span></span> <span data-ttu-id="f90a9-109">Si vous multipliez les éléments du tableau par la largeur de stylet 5, vous recevez {25, 10, 75, 20}.</span><span class="sxs-lookup"><span data-stu-id="f90a9-109">If you multiply the elements of the array by the pen width of 5, you get {25, 10, 75, 20}.</span></span> <span data-ttu-id="f90a9-110">Les tirets alternés sont de longueur comprise entre 25 et 75, tandis que les espaces alternent entre 10 et 20.</span><span class="sxs-lookup"><span data-stu-id="f90a9-110">The displayed dashes alternate in length between 25 and 75, and the spaces alternate in length between 10 and 20.</span></span>


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



<span data-ttu-id="f90a9-111">L’illustration suivante montre la ligne en pointillés résultante.</span><span class="sxs-lookup"><span data-stu-id="f90a9-111">The following illustration shows the resulting dashed line.</span></span> <span data-ttu-id="f90a9-112">Notez que le tiret final doit être inférieur à 25 unités pour que la ligne puisse se terminer à (405, 5).</span><span class="sxs-lookup"><span data-stu-id="f90a9-112">Note that the final dash has to be shorter than 25 units so that the line can end at (405, 5).</span></span>

![Illustration montrant une ligne en pointillés ; chaque segment est une ligne abrégée suivie d’une longue](images/pens6.png)

 

 



