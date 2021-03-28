---
description: 'Vous pouvez activer la correction gamma pour un pinceau de dégradé en passant TRUE à la méthode PathGradientBrush :: SetGammaCorrection de ce pinceau.'
ms.assetid: 47472e41-f469-44f4-8b39-cf3982b79f9e
title: Application d’une correction gamma à un dégradé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e51673e8be4fd289286ce5e4e3e8f7c5469724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115271"
---
# <a name="applying-gamma-correction-to-a-gradient"></a><span data-ttu-id="d519f-103">Application d’une correction gamma à un dégradé</span><span class="sxs-lookup"><span data-stu-id="d519f-103">Applying Gamma Correction to a Gradient</span></span>

<span data-ttu-id="d519f-104">Vous pouvez activer la correction gamma pour un pinceau de dégradé en passant **true** à la méthode [**PathGradientBrush :: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) de ce pinceau.</span><span class="sxs-lookup"><span data-stu-id="d519f-104">You can enable gamma correction for a gradient brush by passing **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method of that brush.</span></span> <span data-ttu-id="d519f-105">Vous pouvez désactiver la correction gamma en passant la **valeur false** à la méthode **PathGradientBrush :: SetGammaCorrection** .</span><span class="sxs-lookup"><span data-stu-id="d519f-105">You can disable gamma correction by passing **FALSE** to the **PathGradientBrush::SetGammaCorrection** method.</span></span> <span data-ttu-id="d519f-106">La correction gamma est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d519f-106">Gamma correction is disabled by default.</span></span>

<span data-ttu-id="d519f-107">L’exemple suivant crée un pinceau de dégradé linéaire et utilise ce pinceau pour remplir deux rectangles.</span><span class="sxs-lookup"><span data-stu-id="d519f-107">The following example creates a linear gradient brush and uses that brush to fill two rectangles.</span></span> <span data-ttu-id="d519f-108">Le premier rectangle est rempli sans correction gamma et le deuxième rectangle est rempli avec la correction gamma.</span><span class="sxs-lookup"><span data-stu-id="d519f-108">The first rectangle is filled without gamma correction and the second rectangle is filled with gamma correction.</span></span>


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // Opaque red
   Color(255, 0, 0, 255));  // Opaque blue

graphics.FillRectangle(&linGrBrush, 0, 0, 200, 50);
linGrBrush.SetGammaCorrection(TRUE);
graphics.FillRectangle(&linGrBrush, 0, 60, 200, 50); 
```



<span data-ttu-id="d519f-109">L’illustration suivante montre les deux rectangles remplis.</span><span class="sxs-lookup"><span data-stu-id="d519f-109">The following illustration shows the two filled rectangles.</span></span> <span data-ttu-id="d519f-110">Le rectangle supérieur, qui n’a pas de correction gamma, apparaît sombre au milieu.</span><span class="sxs-lookup"><span data-stu-id="d519f-110">The top rectangle, which does not have gamma correction, appears dark in the middle.</span></span> <span data-ttu-id="d519f-111">Le rectangle inférieur, qui a une correction gamma, semble avoir une intensité plus uniforme.</span><span class="sxs-lookup"><span data-stu-id="d519f-111">The bottom rectangle, which has gamma correction, appears to have more uniform intensity.</span></span>

![Illustration montrant deux rectangles : le remplissage de couleur de la première varie en fonction de l’intensité, le remplissage de la seconde varie moins](images/gammagradient1.png)

<span data-ttu-id="d519f-113">L’exemple suivant crée un pinceau de dégradé de tracé basé sur un tracé en forme d’étoile.</span><span class="sxs-lookup"><span data-stu-id="d519f-113">The following example creates a path gradient brush based on a star-shaped path.</span></span> <span data-ttu-id="d519f-114">Le code utilise le pinceau de dégradé de tracé avec la correction gamma désactivée (valeur par défaut) pour remplir le tracé.</span><span class="sxs-lookup"><span data-stu-id="d519f-114">The code uses the path gradient brush with gamma correction disabled (the default) to fill the path.</span></span> <span data-ttu-id="d519f-115">Ensuite, le code passe **true** à la méthode [**PathGradientBrush :: SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) pour activer la correction gamma pour le pinceau de dégradé du tracé.</span><span class="sxs-lookup"><span data-stu-id="d519f-115">Then the code passes **TRUE** to the [**PathGradientBrush::SetGammaCorrection**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setgammacorrection) method to enable gamma correction for the path gradient brush.</span></span> <span data-ttu-id="d519f-116">L’appel à [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) définit la transformation universelle d’un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) afin que l’appel suivant à [**Graphics :: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) remplisse une étoile qui se trouve à droite de la première étoile.</span><span class="sxs-lookup"><span data-stu-id="d519f-116">The call to [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) sets the world transformation of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object so that the subsequent call to [**Graphics::FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) fills a star that sits to the right of the first star.</span></span>


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0), Point(100, 50), 
                  Point(150, 50), Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150), Point(37, 75), 
                  Point(0, 50), Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
pthGrBrush.SetGammaCorrection(TRUE);
graphics.TranslateTransform(200.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



<span data-ttu-id="d519f-117">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="d519f-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="d519f-118">L’étoile à droite a une correction gamma.</span><span class="sxs-lookup"><span data-stu-id="d519f-118">The star on the right has gamma correction.</span></span> <span data-ttu-id="d519f-119">Notez que l’étoile sur la gauche, qui n’a pas de correction gamma, a des zones qui apparaissent sombres.</span><span class="sxs-lookup"><span data-stu-id="d519f-119">Note that the star on the left, which does not have gamma correction, has areas that appear dark.</span></span>

![illustration de 2 5-pointé commence par un dégradé de couleur ; la première a des zones sombres, la seconde ne le fait pas](images/gammagradient2.png)

 

 



