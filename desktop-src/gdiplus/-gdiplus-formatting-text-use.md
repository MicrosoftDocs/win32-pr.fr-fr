---
description: Pour appliquer une mise en forme spéciale à du texte, initialisez un objet StringFormat et transmettez l’adresse de cet objet à la méthode DrawString de la classe Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Mise en forme du texte (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553255"
---
# <a name="formatting-text-gdi"></a><span data-ttu-id="31819-103">Mise en forme du texte (GDI+)</span><span class="sxs-lookup"><span data-stu-id="31819-103">Formatting Text (GDI+)</span></span>

<span data-ttu-id="31819-104">Pour appliquer une mise en forme spéciale à du texte, initialisez un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) et transmettez l’adresse de cet objet à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="31819-104">To apply special formatting to text, initialize a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and pass the address of that object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="31819-105">Pour dessiner du texte mis en forme dans un rectangle, vous avez besoin des objets [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)et [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="31819-105">To draw formatted text in a rectangle, you need [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), and [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) objects.</span></span>

-   [<span data-ttu-id="31819-106">Aligner du texte</span><span class="sxs-lookup"><span data-stu-id="31819-106">Aligning Text</span></span>](#aligning-text)
-   [<span data-ttu-id="31819-107">Définir des taquets de tabulation</span><span class="sxs-lookup"><span data-stu-id="31819-107">Setting Tab Stops</span></span>](#setting-tab-stops)
-   [<span data-ttu-id="31819-108">Dessiner du texte vertical</span><span class="sxs-lookup"><span data-stu-id="31819-108">Drawing Vertical Text</span></span>](#drawing-vertical-text)

## <a name="aligning-text"></a><span data-ttu-id="31819-109">Aligner du texte</span><span class="sxs-lookup"><span data-stu-id="31819-109">Aligning Text</span></span>

<span data-ttu-id="31819-110">L’exemple suivant dessine du texte dans un rectangle.</span><span class="sxs-lookup"><span data-stu-id="31819-110">The following example draws text in a rectangle.</span></span> <span data-ttu-id="31819-111">Chaque ligne de texte est centrée (côte à côte) et le bloc de texte entier est centré (de haut en bas) dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="31819-111">Each line of text is centered (side to side), and the entire block of text is centered (top to bottom) in the rectangle.</span></span>


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="31819-112">L’illustration suivante montre le rectangle et le texte centré.</span><span class="sxs-lookup"><span data-stu-id="31819-112">The following illustration shows the rectangle and the centered text.</span></span>

![capture d’écran d’une fenêtre contenant un rectangle, qui contient six lignes de texte, centrées horizontalement](images/fontstext3.png)

<span data-ttu-id="31819-114">Le code précédent appelle deux méthodes de l’objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat :: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) et [**StringFormat :: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span><span class="sxs-lookup"><span data-stu-id="31819-114">The preceding code calls two methods of the [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object: [**StringFormat::SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) and [**StringFormat::SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment).</span></span> <span data-ttu-id="31819-115">L’appel à **StringFormat :: SetAlignment** spécifie que chaque ligne de texte est centrée dans le rectangle donné par le troisième argument passé à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) .</span><span class="sxs-lookup"><span data-stu-id="31819-115">The call to **StringFormat::SetAlignment** specifies that each line of text is centered in the rectangle given by the third argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method.</span></span> <span data-ttu-id="31819-116">L’appel à **StringFormat :: SetLineAlignment** spécifie que le bloc de texte est centré (de haut en bas) dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="31819-116">The call to **StringFormat::SetLineAlignment** specifies that the block of text is centered (top to bottom) in the rectangle.</span></span>

<span data-ttu-id="31819-117">La valeur [\* \* \* \* StringAlignmentCenter \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) \* \* est un élément de l’énumération **StringAlignment** , qui est déclarée dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="31819-117">The value [\*\*\*\*StringAlignmentCenter\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) is an element of the **StringAlignment** enumeration, which is declared in Gdiplusenums.h.</span></span>

## <a name="setting-tab-stops"></a><span data-ttu-id="31819-118">Définir des taquets de tabulation</span><span class="sxs-lookup"><span data-stu-id="31819-118">Setting Tab Stops</span></span>

<span data-ttu-id="31819-119">Vous pouvez définir des taquets de tabulation pour le texte en appelant la méthode [**StringFormat :: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) d’un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) , puis en passant l’adresse de cet objet **StringFormat** à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="31819-119">You can set tab stops for text by calling the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object and then passing the address of that **StringFormat** object to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span>

<span data-ttu-id="31819-120">L’exemple suivant définit des taquets de tabulation à 150, 250 et 350.</span><span class="sxs-lookup"><span data-stu-id="31819-120">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="31819-121">Ensuite, le code affiche une liste avec onglets de noms et de scores de test.</span><span class="sxs-lookup"><span data-stu-id="31819-121">Then the code displays a tabbed list of names and test scores.</span></span>


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



<span data-ttu-id="31819-122">L’illustration suivante montre le texte avec onglets.</span><span class="sxs-lookup"><span data-stu-id="31819-122">The following illustration shows the tabbed text.</span></span>

![illustration d’un rectangle contenant quatre colonnes de texte ; chaque colonne est redéfinie à gauche](images/fontstext4.png)

<span data-ttu-id="31819-124">Le code précédent passe trois arguments à la méthode [**StringFormat :: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) .</span><span class="sxs-lookup"><span data-stu-id="31819-124">The preceding code passes three arguments to the [**StringFormat::SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) method.</span></span> <span data-ttu-id="31819-125">Le troisième argument est l’adresse d’un tableau contenant les décalages de tabulation.</span><span class="sxs-lookup"><span data-stu-id="31819-125">The third argument is the address of an array containing the tab offsets.</span></span> <span data-ttu-id="31819-126">Le deuxième argument indique qu’il y a trois décalages dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="31819-126">The second argument indicates that there are three offsets in that array.</span></span> <span data-ttu-id="31819-127">Le premier argument passé à **StringFormat :: SetTabStops** est 0, ce qui indique que le premier décalage dans le tableau est mesuré à partir de la position 0, le bord gauche du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="31819-127">The first argument passed to **StringFormat::SetTabStops** is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>

## <a name="drawing-vertical-text"></a><span data-ttu-id="31819-128">Dessiner du texte vertical</span><span class="sxs-lookup"><span data-stu-id="31819-128">Drawing Vertical Text</span></span>

<span data-ttu-id="31819-129">Vous pouvez utiliser un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) pour spécifier que le texte doit être dessiné verticalement plutôt que horizontalement.</span><span class="sxs-lookup"><span data-stu-id="31819-129">You can use a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object to specify that text be drawn vertically rather than horizontally.</span></span>

<span data-ttu-id="31819-130">L’exemple suivant passe la valeur [\* \* \* \* StringFormatFlagsDirectionVertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* à la méthode [**StringFormat :: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) d’un objet [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) .</span><span class="sxs-lookup"><span data-stu-id="31819-130">The following example passes the value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) to the [**StringFormat::SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) method of a [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) object.</span></span> <span data-ttu-id="31819-131">L’adresse de cet objet **StringFormat** est passée à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="31819-131">The address of that **StringFormat** object is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="31819-132">La valeur [\* \* \* \* StringFormatFlagsDirectionVertical \* \*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) \* \* est un élément de l’énumération **StringFormatFlags** , qui est déclarée dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="31819-132">The value [\*\*\*\*StringFormatFlagsDirectionVertical\*\*\*\*](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) is an element of the **StringFormatFlags** enumeration, which is declared in Gdiplusenums.h.</span></span>


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



<span data-ttu-id="31819-133">L’illustration suivante montre le texte vertical.</span><span class="sxs-lookup"><span data-stu-id="31819-133">The following illustration shows the vertical text.</span></span>

![Illustration montrant une fenêtre contenant du texte pivoté de 90 degrés dans le sens des aiguilles d’une montre](images/fontstext5.png)

 

 



