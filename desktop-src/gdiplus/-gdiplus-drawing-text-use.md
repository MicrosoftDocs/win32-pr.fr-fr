---
description: Vous pouvez utiliser la méthode DrawString de la classe Graphics pour dessiner du texte à un emplacement spécifié ou dans un rectangle spécifié.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Dessiner du texte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16ed49a5ab92380b42ed3316346ac547f95be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115231"
---
# <a name="drawing-text-gdi"></a><span data-ttu-id="a96d8-103">Dessiner du texte (GDI+)</span><span class="sxs-lookup"><span data-stu-id="a96d8-103">Drawing Text (GDI+)</span></span>

<span data-ttu-id="a96d8-104">Vous pouvez utiliser la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) pour dessiner du texte à un emplacement spécifié ou dans un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a96d8-104">You can use the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw text at a specified location or within a specified rectangle.</span></span>

-   [<span data-ttu-id="a96d8-105">Dessin de texte à un emplacement spécifié</span><span class="sxs-lookup"><span data-stu-id="a96d8-105">Drawing Text at a Specified Location</span></span>](#drawing-text-at-a-specified-location)
-   [<span data-ttu-id="a96d8-106">Dessiner du texte dans un rectangle</span><span class="sxs-lookup"><span data-stu-id="a96d8-106">Drawing Text in a Rectangle</span></span>](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a><span data-ttu-id="a96d8-107">Dessin de texte à un emplacement spécifié</span><span class="sxs-lookup"><span data-stu-id="a96d8-107">Drawing Text at a Specified Location</span></span>

<span data-ttu-id="a96d8-108">Pour dessiner du texte à un emplacement spécifié, vous avez besoin d’objets [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)et [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="a96d8-108">To draw text at a specified location, you need [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="a96d8-109">L’exemple suivant dessine la chaîne « Hello » à l’emplacement (30, 10).</span><span class="sxs-lookup"><span data-stu-id="a96d8-109">The following example draws the string "Hello" at location (30, 10).</span></span> <span data-ttu-id="a96d8-110">La famille de polices est Times New Roman.</span><span class="sxs-lookup"><span data-stu-id="a96d8-110">The font family is Times New Roman.</span></span> <span data-ttu-id="a96d8-111">La police, qui est un membre individuel de la famille de polices, est Times New Roman, taille 24 pixels, style normal.</span><span class="sxs-lookup"><span data-stu-id="a96d8-111">The font, which is an individual member of the font family, is Times New Roman, size 24 pixels, regular style.</span></span> <span data-ttu-id="a96d8-112">Supposons que **Graphics** est un objet [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existant.</span><span class="sxs-lookup"><span data-stu-id="a96d8-112">Assume that **graphics** is an existing [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

<span data-ttu-id="a96d8-113">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="a96d8-113">The following illustration shows the output of the preceding code.</span></span>

![capture d’écran d’une petite fenêtre contenant le texte « Hello »](images/fontstext1.png)

<span data-ttu-id="a96d8-115">Dans l’exemple précédent, le constructeur [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) reçoit une chaîne qui identifie la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="a96d8-115">In the preceding example, the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a string that identifies the font family.</span></span> <span data-ttu-id="a96d8-116">L’adresse de l’objet **FontFamily** est passée comme premier argument au constructeur [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="a96d8-116">The address of the **FontFamily** object is passed as the first argument to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="a96d8-117">Le deuxième argument passé au constructeur **font** spécifie la taille de la police mesurée dans les unités fournies par le quatrième argument.</span><span class="sxs-lookup"><span data-stu-id="a96d8-117">The second argument passed to the **Font** constructor specifies the size of the font measured in units given by the fourth argument.</span></span> <span data-ttu-id="a96d8-118">Le troisième argument spécifie le style (normal, gras, italique, etc.) de la police.</span><span class="sxs-lookup"><span data-stu-id="a96d8-118">The third argument specifies the style (regular, bold, italic, and so on) of the font.</span></span>

<span data-ttu-id="a96d8-119">La méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) reçoit cinq arguments.</span><span class="sxs-lookup"><span data-stu-id="a96d8-119">The [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method receives five arguments.</span></span> <span data-ttu-id="a96d8-120">Le premier argument est la chaîne à dessiner et le deuxième argument est la longueur (en caractères, et non en octets) de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="a96d8-120">The first argument is the string to be drawn, and the second argument is the length (in characters, not bytes) of that string.</span></span> <span data-ttu-id="a96d8-121">Si la chaîne se termine par un caractère null, vous pouvez passer-1 pour la longueur.</span><span class="sxs-lookup"><span data-stu-id="a96d8-121">If the string is null-terminated, you can pass –1 for the length.</span></span> <span data-ttu-id="a96d8-122">Le troisième argument est l’adresse de l’objet [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) qui a été construit précédemment.</span><span class="sxs-lookup"><span data-stu-id="a96d8-122">The third argument is the address of the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object that was constructed previously.</span></span> <span data-ttu-id="a96d8-123">Le quatrième argument est un objet [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) qui contient les coordonnées de l’angle supérieur gauche de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a96d8-123">The fourth argument is a [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) object that contains the coordinates of the upper-left corner of the string.</span></span> <span data-ttu-id="a96d8-124">Le cinquième argument est l’adresse d’un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) qui sera utilisé pour remplir les caractères de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="a96d8-124">The fifth argument is the address of a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object that will be used to fill the characters of the string.</span></span>

## <a name="drawing-text-in-a-rectangle"></a><span data-ttu-id="a96d8-125">Dessiner du texte dans un rectangle</span><span class="sxs-lookup"><span data-stu-id="a96d8-125">Drawing Text in a Rectangle</span></span>

<span data-ttu-id="a96d8-126">L’une des méthodes [**DrawString**](https://www.bing.com/search?q=**DrawString**) de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a un paramètre *RectF* .</span><span class="sxs-lookup"><span data-stu-id="a96d8-126">One of the [**DrawString**](https://www.bing.com/search?q=**DrawString**) methods of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has a *RectF* parameter.</span></span> <span data-ttu-id="a96d8-127">En appelant cette méthode **DrawString** , vous pouvez dessiner du texte encapsulé dans un rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a96d8-127">By calling that **DrawString** method, you can draw text that wraps in a specified rectangle.</span></span> <span data-ttu-id="a96d8-128">Pour dessiner du texte dans un rectangle, vous avez besoin des objets **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)et [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="a96d8-128">To draw text in a rectangle, you need **Graphics**, [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf), and [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

<span data-ttu-id="a96d8-129">L’exemple suivant crée un rectangle avec l’angle supérieur gauche (30, 10), la largeur 100 et la hauteur 122.</span><span class="sxs-lookup"><span data-stu-id="a96d8-129">The following example creates a rectangle with upper-left corner (30, 10), width 100, and height 122.</span></span> <span data-ttu-id="a96d8-130">Le code dessine ensuite une chaîne à l’intérieur de ce rectangle.</span><span class="sxs-lookup"><span data-stu-id="a96d8-130">Then the code draws a string inside that rectangle.</span></span> <span data-ttu-id="a96d8-131">La chaîne est limitée au rectangle et s’encapsule de telle sorte que les mots individuels ne sont pas rompus.</span><span class="sxs-lookup"><span data-stu-id="a96d8-131">The string is restricted to the rectangle and wraps in such a way that individual words are not broken.</span></span>

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

<span data-ttu-id="a96d8-132">L’illustration suivante montre le texte dessiné dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="a96d8-132">The following illustration shows the text drawn in the rectangle.</span></span>

![capture d’écran d’une petite fenêtre contenant un recangle, dans laquelle apparaît la première partie d’une phrase](images/fontstext2.png)

<span data-ttu-id="a96d8-134">Dans l’exemple précédent, le quatrième argument passé à la méthode [**DrawString**](https://www.bing.com/search?q=**DrawString**) est un objet [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) qui spécifie le rectangle englobant du texte.</span><span class="sxs-lookup"><span data-stu-id="a96d8-134">In the preceding example, the fourth argument passed to the [**DrawString**](https://www.bing.com/search?q=**DrawString**) method is a [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) object that specifies the bounding rectangle for the text.</span></span> <span data-ttu-id="a96d8-135">Le cinquième paramètre est de type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat): l’argument a la **valeur null** , car aucune mise en forme de chaîne spéciale n’est requise.</span><span class="sxs-lookup"><span data-stu-id="a96d8-135">The fifth parameter is of type [**StringFormat**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)— the argument is **NULL** because no special string formatting is required.</span></span>
