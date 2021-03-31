---
description: La rubrique dessine une ligne montre comment écrire une application Windows qui utilise GDI+ pour dessiner une ligne.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Dessin d’une chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202427"
---
# <a name="drawing-a-string"></a><span data-ttu-id="37bfa-103">Dessin d’une chaîne</span><span class="sxs-lookup"><span data-stu-id="37bfa-103">Drawing a String</span></span>

<span data-ttu-id="37bfa-104">La rubrique [dessine une ligne](-gdiplus-drawing-a-line-use.md) montre comment écrire une application Windows qui utilise GDI+ pour dessiner une ligne.</span><span class="sxs-lookup"><span data-stu-id="37bfa-104">The topic [Drawing a Line](-gdiplus-drawing-a-line-use.md) shows how to write a Windows application that uses Windows GDI+ to draw a line.</span></span> <span data-ttu-id="37bfa-105">Pour dessiner une chaîne, remplacez la fonction **OnPaint** présentée dans cette rubrique par la fonction **OnPaint** suivante :</span><span class="sxs-lookup"><span data-stu-id="37bfa-105">To draw a string, replace the **OnPaint** function shown in that topic with the following **OnPaint** function:</span></span>


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



<span data-ttu-id="37bfa-106">Le code précédent crée plusieurs objets GDI+.</span><span class="sxs-lookup"><span data-stu-id="37bfa-106">The previous code creates several GDI+ objects.</span></span> <span data-ttu-id="37bfa-107">L’objet [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) fournit la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , qui effectue le dessin réel.</span><span class="sxs-lookup"><span data-stu-id="37bfa-107">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method, which does the actual drawing.</span></span> <span data-ttu-id="37bfa-108">L’objet [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) spécifie la couleur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="37bfa-108">The [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object specifies the color of the string.</span></span>

<span data-ttu-id="37bfa-109">Le constructeur [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) reçoit un argument de chaîne unique qui identifie la famille de polices.</span><span class="sxs-lookup"><span data-stu-id="37bfa-109">The [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) constructor receives a single, string argument that identifies the font family.</span></span> <span data-ttu-id="37bfa-110">L’adresse de l’objet **FontFamily** est le premier argument passé au constructeur [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="37bfa-110">The address of the **FontFamily** object is the first argument passed to the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) constructor.</span></span> <span data-ttu-id="37bfa-111">Le deuxième argument passé au constructeur [font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) spécifie la taille de la police et le troisième argument spécifie le style.</span><span class="sxs-lookup"><span data-stu-id="37bfa-111">The second argument passed to the [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) constructor specifies the font size, and the third argument specifies the style.</span></span> <span data-ttu-id="37bfa-112">La valeur **FontStyleRegular** est un membre de l’énumération [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , qui est déclarée dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="37bfa-112">The value **FontStyleRegular** is a member of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span> <span data-ttu-id="37bfa-113">Le dernier argument du constructeur **font** indique que la taille de la police (24 dans ce cas) est mesurée en pixels.</span><span class="sxs-lookup"><span data-stu-id="37bfa-113">The last argument to the **Font** constructor indicates that the size of the font (24 in this case) is measured in pixels.</span></span> <span data-ttu-id="37bfa-114">La valeur **UnitPixel** est un membre de l’énumération d' [**unités**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .</span><span class="sxs-lookup"><span data-stu-id="37bfa-114">The value **UnitPixel** is a member of the [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) enumeration.</span></span>

<span data-ttu-id="37bfa-115">Le premier argument passé à la méthode [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) est l’adresse d’une chaîne de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="37bfa-115">The first argument passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method is the address of a wide-character string.</span></span> <span data-ttu-id="37bfa-116">Le deuxième argument,-1, spécifie que la chaîne se termine par une valeur null.</span><span class="sxs-lookup"><span data-stu-id="37bfa-116">The second argument, –1, specifies that the string is null terminated.</span></span> <span data-ttu-id="37bfa-117">(Si la chaîne ne se termine pas par null, le deuxième argument doit spécifier le nombre de caractères larges dans la chaîne.) Le troisième argument est l’adresse de l’objet [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="37bfa-117">(If the string is not null terminated, the second argument should specify the number of wide characters in the string.) The third argument is the address of the [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="37bfa-118">Le quatrième argument est une référence à un objet [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) qui spécifie l’emplacement où la chaîne sera dessinée.</span><span class="sxs-lookup"><span data-stu-id="37bfa-118">The fourth argument is a reference to a [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) object that specifies the location where the string will be drawn.</span></span> <span data-ttu-id="37bfa-119">Le dernier argument est l’adresse de l’objet [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , qui spécifie la couleur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="37bfa-119">The last argument is the address of the [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) object, which specifies the color of the string.</span></span>

 

 
