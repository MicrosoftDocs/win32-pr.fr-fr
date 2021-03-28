---
description: Windows GDI+ fournit plusieurs classes qui constituent la base pour dessiner du texte.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Utilisation du texte et des polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526056"
---
# <a name="using-text-and-fonts"></a><span data-ttu-id="2c54b-103">Utilisation du texte et des polices</span><span class="sxs-lookup"><span data-stu-id="2c54b-103">Using Text and Fonts</span></span>

<span data-ttu-id="2c54b-104">Windows GDI+ fournit plusieurs classes qui constituent la base pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="2c54b-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="2c54b-105">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) possède plusieurs méthodes [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) qui vous permettent de spécifier différentes fonctionnalités de texte, telles que l’emplacement, le rectangle englobant, la police et le format.</span><span class="sxs-lookup"><span data-stu-id="2c54b-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="2c54b-106">Les autres classes qui contribuent à la restitution du texte incluent notamment [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)et [**la**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="2c54b-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="2c54b-107">Les rubriques suivantes traitent du texte et des polices plus en détail :</span><span class="sxs-lookup"><span data-stu-id="2c54b-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="2c54b-108">Construction des familles de polices et des polices</span><span class="sxs-lookup"><span data-stu-id="2c54b-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="2c54b-109">Dessiner du texte</span><span class="sxs-lookup"><span data-stu-id="2c54b-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="2c54b-110">Mise en forme du texte</span><span class="sxs-lookup"><span data-stu-id="2c54b-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="2c54b-111">Énumération des polices installées</span><span class="sxs-lookup"><span data-stu-id="2c54b-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="2c54b-112">Création de collections de polices privées</span><span class="sxs-lookup"><span data-stu-id="2c54b-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="2c54b-113">Obtention de métriques de police</span><span class="sxs-lookup"><span data-stu-id="2c54b-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="2c54b-114">Anticrénelage avec du texte</span><span class="sxs-lookup"><span data-stu-id="2c54b-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



