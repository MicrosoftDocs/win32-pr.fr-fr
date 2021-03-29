---
description: 'Il peut arriver que vous souhaitiez créer une image bitmap hors écran qui présente les caractéristiques suivantes :'
ms.assetid: 2a7590ce-daf4-4892-a838-603e3f89b1bb
title: Utilisation du mode de composition pour contrôler la fusion alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db54c71ac9687a1ddf28db09b922b7799d0ebaa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972827"
---
# <a name="using-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="0b8d0-103">Utilisation du mode de composition pour contrôler la fusion alpha</span><span class="sxs-lookup"><span data-stu-id="0b8d0-103">Using Compositing Mode to Control Alpha Blending</span></span>

<span data-ttu-id="0b8d0-104">Il peut arriver que vous souhaitiez créer une image bitmap hors écran qui présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b8d0-104">There might be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>

-   <span data-ttu-id="0b8d0-105">Les couleurs ont des valeurs alpha inférieures à 255.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-105">Colors have alpha values that are less than 255.</span></span>
-   <span data-ttu-id="0b8d0-106">Les couleurs ne sont pas fusionnées entre elles lorsque vous créez l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-106">Colors are not alpha blended with each other as you create the bitmap.</span></span>
-   <span data-ttu-id="0b8d0-107">Lorsque vous affichez la bitmap terminée, les couleurs de la bitmap sont fusionnées alpha avec les couleurs d’arrière-plan sur le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-107">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>

<span data-ttu-id="0b8d0-108">Pour créer une telle image bitmap, construisez un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) vide, puis construisez un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur cette image bitmap.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-108">To create such a bitmap, construct a blank [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object, and then construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on that bitmap.</span></span> <span data-ttu-id="0b8d0-109">Définissez le mode de composition de l’objet **Graphics** sur CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-109">Set the compositing mode of the **Graphics** object to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="0b8d0-110">L’exemple suivant crée un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un objet [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) .</span><span class="sxs-lookup"><span data-stu-id="0b8d0-110">The following example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="0b8d0-111">Le code utilise l’objet **Graphics** avec deux pinceaux translucides (alpha = 160) pour peindre sur l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-111">The code uses the **Graphics** object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="0b8d0-112">Le code remplit une ellipse rouge et une ellipse verte à l’aide des pinceaux translucides.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="0b8d0-113">L’ellipse verte chevauche l’ellipse rouge, mais le vert n’est pas mélangé au rouge, car le mode de composition de l’objet **Graphics** est défini sur CompositingModeSourceCopy.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the **Graphics** object is set to CompositingModeSourceCopy.</span></span>

<span data-ttu-id="0b8d0-114">Ensuite, le code se prépare à dessiner à l’écran en appelant [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) et en créant un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basé sur un contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-114">Next the code prepares to draw on the screen by calling [BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) and creating a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a device context.</span></span> <span data-ttu-id="0b8d0-115">Le code dessine le bitmap à l’écran deux fois : une fois sur un arrière-plan blanc et une fois sur un arrière-plan multicolore.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-115">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="0b8d0-116">Les pixels de l’image bitmap qui font partie des deux points de suspension ont un composant alpha de 160, de sorte que les points de suspension sont fusionnés avec les couleurs d’arrière-plan de l’écran.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-116">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>


```
// Create a blank bitmap.
Bitmap bitmap(180, 100);
// Create a Graphics object that can be used to draw on the bitmap.
Graphics bitmapGraphics(&bitmap);
// Create a red brush and a green brush, each with an alpha value of 160.
SolidBrush redBrush(Color(210, 255, 0, 0));
SolidBrush greenBrush(Color(210, 0, 255, 0));
// Set the compositing mode so that when overlapping ellipses are drawn,
// the colors of the ellipses are not blended.
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
// Fill an ellipse using a red brush that has an alpha value of 160.
bitmapGraphics.FillEllipse(&redBrush, 0, 0, 150, 70);
// Fill a second ellipse using green brush that has an alpha value of 160. 
// The green ellipse overlaps the red ellipse, but the green is not 
// blended with the red.
bitmapGraphics.FillEllipse(&greenBrush, 30, 30, 150, 70);
// Prepare to draw on the screen.
hdc = BeginPaint(hWnd, &ps);
Graphics* pGraphics = new Graphics(hdc);
pGraphics->SetCompositingQuality(CompositingQualityGammaCorrected);
// Draw a multicolored background.
SolidBrush brush(Color((ARGB)Color::Aqua));
pGraphics->FillRectangle(&brush, 200, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Yellow));
pGraphics->FillRectangle(&brush, 260, 0, 60, 100);
brush.SetColor(Color((ARGB)Color::Fuchsia));
pGraphics->FillRectangle(&brush, 320, 0, 60, 100);
   
// Display the bitmap on a white background.
pGraphics->DrawImage(&bitmap, 0, 0);
// Display the bitmap on a multicolored background.
pGraphics->DrawImage(&bitmap, 200, 0);
delete pGraphics;
EndPaint(hWnd, &ps);
```



<span data-ttu-id="0b8d0-117">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-117">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="0b8d0-118">Notez que les ellipses sont fusionnées avec l’arrière-plan, mais elles ne sont pas fusionnées les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-118">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>

![Illustration montrant deux ellipses de couleur différente, chacune d’entre elles fondue avec son arrière-plan multicolore](images/sourcecopy.png)

<span data-ttu-id="0b8d0-120">L’exemple de code précédent contient l’instruction suivante :</span><span class="sxs-lookup"><span data-stu-id="0b8d0-120">The preceding code example has the following statement:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceCopy);
```



<span data-ttu-id="0b8d0-121">Si vous souhaitez que les ellipses soient fusionnées les unes avec les autres, et avec l’arrière-plan, remplacez cette instruction par ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="0b8d0-121">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>


```
bitmapGraphics.SetCompositingMode(CompositingModeSourceOver);
```



<span data-ttu-id="0b8d0-122">L’illustration suivante montre la sortie du code modifié.</span><span class="sxs-lookup"><span data-stu-id="0b8d0-122">The following illustration shows the output of the revised code.</span></span>

![utilisation du mode de composition pour contrôler l’illustration de la fusion alpha](images/sourceover.png)

 

 



