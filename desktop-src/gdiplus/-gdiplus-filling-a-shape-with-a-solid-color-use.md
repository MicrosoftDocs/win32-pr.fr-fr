---
description: Pour remplir une forme avec une couleur unie, créez un objet SolidBrush, puis transmettez l’adresse de cet objet SolidBrush en tant qu’argument à l’une des méthodes de remplissage de la classe Graphics.
ms.assetid: cedef138-5047-4a72-8b89-5a95062a351c
title: Remplissage d’une forme avec une couleur unie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4a6221d84c4a891d377d974f168468917799e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991353"
---
# <a name="filling-a-shape-with-a-solid-color"></a><span data-ttu-id="a4f27-103">Remplissage d’une forme avec une couleur unie</span><span class="sxs-lookup"><span data-stu-id="a4f27-103">Filling a Shape with a Solid Color</span></span>

<span data-ttu-id="a4f27-104">Pour remplir une forme avec une couleur unie, créez un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) , puis transmettez l’adresse de cet objet **SolidBrush** en tant qu’argument à l’une des méthodes de remplissage de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="a4f27-104">To fill a shape with a solid color, create a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object, and then pass the address of that **SolidBrush** object as an argument to one of the fill methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="a4f27-105">L’exemple suivant montre comment remplir une ellipse avec la couleur rouge :</span><span class="sxs-lookup"><span data-stu-id="a4f27-105">The following example shows how to fill an ellipse with the color red:</span></span>


```
SolidBrush solidBrush(Color(255, 255, 0, 0));
stat = graphics.FillEllipse(&solidBrush, 0, 0, 100, 60);
```



<span data-ttu-id="a4f27-106">Dans l’exemple précédent, le constructeur [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) prend une référence d’objet [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) comme seul argument.</span><span class="sxs-lookup"><span data-stu-id="a4f27-106">In the preceding example, the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) constructor takes a [**Color**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) object reference as its only argument.</span></span> <span data-ttu-id="a4f27-107">Les valeurs utilisées par le constructeur de **couleur** représentent les composants alpha, rouge, vert et bleu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="a4f27-107">The values used by the **Color** constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="a4f27-108">Chacune de ces valeurs doit être comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="a4f27-108">Each of these values must be in the range 0 through 255.</span></span> <span data-ttu-id="a4f27-109">Le premier 255 indique que la couleur est entièrement opaque, tandis que le deuxième 255 indique que le composant rouge est en intensité complète.</span><span class="sxs-lookup"><span data-stu-id="a4f27-109">The first 255 indicates that the color is fully opaque, and the second 255 indicates that the red component is at full intensity.</span></span> <span data-ttu-id="a4f27-110">Les deux zéros indiquent que les composants vert et bleu ont tous les deux une intensité égale à 0.</span><span class="sxs-lookup"><span data-stu-id="a4f27-110">The two zeros indicate that the green and blue components both have an intensity of 0.</span></span>

<span data-ttu-id="a4f27-111">Les quatre nombres (0, 0, 100, 60) passés à la méthode [**Graphics :: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) spécifient l’emplacement et la taille du rectangle englobant pour l’ellipse.</span><span class="sxs-lookup"><span data-stu-id="a4f27-111">The four numbers (0, 0, 100, 60) passed to the [**Graphics::FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inint_inint_inint_inint)) method specify the location and size of the bounding rectangle for the ellipse.</span></span> <span data-ttu-id="a4f27-112">Le rectangle a un angle supérieur gauche de (0,0), une largeur de 100 et une hauteur de 60.</span><span class="sxs-lookup"><span data-stu-id="a4f27-112">The rectangle has an upper-left corner of (0, 0), a width of 100, and a height of 60.</span></span>

 

 
