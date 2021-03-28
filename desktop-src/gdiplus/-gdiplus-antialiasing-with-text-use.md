---
description: Windows GDI+ fournit différents niveaux de qualité pour dessiner du texte. En règle générale, un rendu de qualité supérieure prend plus de temps de traitement que le rendu de qualité inférieure.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Anticrénelage avec du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991453"
---
# <a name="antialiasing-with-text"></a><span data-ttu-id="b6ff0-104">Anticrénelage avec du texte</span><span class="sxs-lookup"><span data-stu-id="b6ff0-104">Antialiasing with Text</span></span>

<span data-ttu-id="b6ff0-105">Windows GDI+ fournit différents niveaux de qualité pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-105">Windows GDI+ provides various quality levels for drawing text.</span></span> <span data-ttu-id="b6ff0-106">En règle générale, un rendu de qualité supérieure prend plus de temps de traitement que le rendu de qualité inférieure.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-106">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span>

<span data-ttu-id="b6ff0-107">Le niveau de qualité est une propriété de la classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="b6ff0-107">The quality level is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="b6ff0-108">Pour définir le niveau de qualité, appelez la méthode [**Graphics :: SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) d’un objet **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="b6ff0-108">To set the quality level, call the [**Graphics::SetTextRenderingHint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) method of a **Graphics** object.</span></span> <span data-ttu-id="b6ff0-109">La méthode **Graphics :: SetTextRenderingHint** reçoit l’un des éléments de l’énumération [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) , qui est déclarée dans Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-109">The **Graphics::SetTextRenderingHint** method receives one of the elements of the [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="b6ff0-110">GDI+ fournit un anticrénelage traditionnel et un nouveau type d’anticrénelage basé sur la technologie d’affichage Microsoft ClearType uniquement disponible sur Windows XP et Windows Server 2003 et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-110">GDI+ provides traditional antialiasing and a new kind of antialiasing based on Microsoft ClearType display technology only available on Windows XP and Windows Server 2003 and later versions of Windows.</span></span> <span data-ttu-id="b6ff0-111">Le lissage ClearType améliore la lisibilité sur les moniteurs LCD couleur qui ont une interface numérique, comme les moniteurs des ordinateurs portables et les écrans plats de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-111">ClearType smoothing improves readability on color LCD monitors that have a digital interface, such as the monitors in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="b6ff0-112">La lisibilité sur les écrans CRT est également un peu améliorée.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-112">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="b6ff0-113">ClearType dépend de l’orientation et de l’ordre des bandes LCD.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-113">ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="b6ff0-114">À l’heure actuelle, ClearType est implémenté uniquement pour les bandes verticales qui sont triées RVB.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-114">Currently, ClearType is implemented only for vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="b6ff0-115">Cela peut être un problème si vous utilisez un Tablet PC, où l’affichage peut être orienté dans n’importe quelle direction ou si vous utilisez un écran qui peut être converti en mode portrait.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-115">This might be a concern if you are using a tablet PC, where the display can be oriented in any direction, or if you are using a screen that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="b6ff0-116">L’exemple suivant dessine du texte avec deux paramètres de qualité différents :</span><span class="sxs-lookup"><span data-stu-id="b6ff0-116">The following example draws text with two different quality settings:</span></span>


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



<span data-ttu-id="b6ff0-117">L’illustration suivante montre la sortie du code précédent.</span><span class="sxs-lookup"><span data-stu-id="b6ff0-117">The following illustration shows the output of the preceding code.</span></span>

![capture d’écran d’une chaîne dont les caractères ont des bords dentelés et un avec des bords lisses](images/fontstext10.png)

 

 



