---
description: Vous pouvez utiliser un pinceau dégradé pour remplir une forme avec une couleur à variation progressive.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Remplissage de formes à l’aide d’un pinceau dégradé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991349"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="7ff83-103">Remplissage de formes à l’aide d’un pinceau dégradé</span><span class="sxs-lookup"><span data-stu-id="7ff83-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="7ff83-104">Vous pouvez utiliser un pinceau dégradé pour remplir une forme avec une couleur à variation progressive.</span><span class="sxs-lookup"><span data-stu-id="7ff83-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="7ff83-105">Par exemple, vous pouvez utiliser un dégradé horizontal pour remplir une forme avec une couleur qui change graduellement à mesure que vous vous déplacez du bord gauche de la forme vers le bord droit.</span><span class="sxs-lookup"><span data-stu-id="7ff83-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="7ff83-106">Imaginez un rectangle avec un bord gauche noir (représenté par les composants rouge, vert et bleu 0, 0, 0) et un bord droit rouge (représenté par 255, 0,0).</span><span class="sxs-lookup"><span data-stu-id="7ff83-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="7ff83-107">Si le rectangle a une largeur de 256 pixels, le composant rouge d’un pixel donné sera supérieur au composant rouge du pixel à sa gauche.</span><span class="sxs-lookup"><span data-stu-id="7ff83-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="7ff83-108">Le pixel le plus à gauche d’une ligne possède des composants de couleur (0, 0, 0), le deuxième pixel a (1,0), le troisième pixel a (2, 0, 0), et ainsi de suite, jusqu’à ce que vous obteniez le pixel le plus à droite, qui a des composants de couleur (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="7ff83-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="7ff83-109">Ces valeurs de couleur interpolées composent le dégradé de couleur.</span><span class="sxs-lookup"><span data-stu-id="7ff83-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="7ff83-110">Un dégradé linéaire change de couleur lorsque vous le déplacez horizontalement, verticalement ou parallèlement à une ligne inclinée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7ff83-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="7ff83-111">Un dégradé de tracé change de couleur à mesure que vous dépassez l’intérieur et la limite d’un tracé.</span><span class="sxs-lookup"><span data-stu-id="7ff83-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="7ff83-112">Vous pouvez personnaliser les dégradés de tracés pour obtenir un grand nombre d’effets.</span><span class="sxs-lookup"><span data-stu-id="7ff83-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="7ff83-113">GDI+ fournit les classes [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) et [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , qui héritent toutes deux de la classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="7ff83-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="7ff83-114">Les rubriques suivantes traitent des dégradés linéaires et de tracés plus en détail :</span><span class="sxs-lookup"><span data-stu-id="7ff83-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="7ff83-115">Création d’un dégradé linéaire</span><span class="sxs-lookup"><span data-stu-id="7ff83-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="7ff83-116">Création d’un dégradé de tracé</span><span class="sxs-lookup"><span data-stu-id="7ff83-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="7ff83-117">Application d’une correction gamma à un dégradé</span><span class="sxs-lookup"><span data-stu-id="7ff83-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



