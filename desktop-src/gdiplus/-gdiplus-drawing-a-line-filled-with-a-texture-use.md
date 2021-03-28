---
description: Au lieu de dessiner une ligne ou une courbe avec une couleur unie, vous pouvez dessiner avec une texture.
ms.assetid: 326170a5-d21f-49d6-9f60-10b9bc8d97b4
title: Dessin d’une ligne remplie d’une texture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf6a061399791009fd7c1b645bb09dbba25362f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972898"
---
# <a name="drawing-a-line-filled-with-a-texture"></a><span data-ttu-id="81df6-103">Dessin d’une ligne remplie d’une texture</span><span class="sxs-lookup"><span data-stu-id="81df6-103">Drawing a Line Filled with a Texture</span></span>

<span data-ttu-id="81df6-104">Au lieu de dessiner une ligne ou une courbe avec une couleur unie, vous pouvez dessiner avec une texture.</span><span class="sxs-lookup"><span data-stu-id="81df6-104">Instead of drawing a line or curve with a solid color, you can draw with a texture.</span></span> <span data-ttu-id="81df6-105">Pour dessiner des lignes et des courbes avec une texture, créez un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) et transmettez l’adresse de cet objet **TextureBrush** à un constructeur [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="81df6-105">To draw lines and curves with a texture, create a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and pass the address of that **TextureBrush** object to a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) constructor.</span></span> <span data-ttu-id="81df6-106">L’image associée au pinceau de texture est utilisée pour juxtaposer le plan (de façon invisible) et, lorsque le stylet dessine une ligne ou une courbe, le trait du stylet dévoile certains pixels de la texture en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="81df6-106">The image associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>

<span data-ttu-id="81df6-107">L’exemple suivant crée un objet [**image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) à partir du fichier Texture1.jpg.</span><span class="sxs-lookup"><span data-stu-id="81df6-107">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the file Texture1.jpg.</span></span> <span data-ttu-id="81df6-108">Cette image est utilisée pour construire un objet [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) , et l’objet **TextureBrush** est utilisé pour construire un objet [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) .</span><span class="sxs-lookup"><span data-stu-id="81df6-108">That image is used to construct a [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush) object, and the **TextureBrush** object is used to construct a [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) object.</span></span> <span data-ttu-id="81df6-109">L’appel à [**Graphics ::D rawimage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) dessine l’image avec son coin supérieur gauche à (0,0).</span><span class="sxs-lookup"><span data-stu-id="81df6-109">The call to [**Graphics::DrawImage**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inint_inint_inint_inint)) draws the image with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="81df6-110">L’appel à [**Graphics ::D rawellipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) utilise l’objet **Pen** pour dessiner une ellipse texturée.</span><span class="sxs-lookup"><span data-stu-id="81df6-110">The call to [**Graphics::DrawEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) uses the **Pen** object to draw a textured ellipse.</span></span>


```
Image         image(L"Texture1.jpg");
TextureBrush  tBrush(&image);
Pen           texturedPen(&tBrush, 30);

graphics.DrawImage(&image, 0, 0, image.GetWidth(), image.GetHeight());
graphics.DrawEllipse(&texturedPen, 100, 20, 200, 100);
```



<span data-ttu-id="81df6-111">L’illustration suivante montre l’image et l’ellipse texturée.</span><span class="sxs-lookup"><span data-stu-id="81df6-111">The following illustration shows the image and the textured ellipse.</span></span>

![Illustration montrant une petite image rectangulaire, puis un segment de ligne elliptique rempli avec l’image d’origine](images/pens7.png)

 

 
