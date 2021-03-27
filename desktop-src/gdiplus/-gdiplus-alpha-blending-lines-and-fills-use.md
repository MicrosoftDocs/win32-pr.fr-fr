---
description: Dans Windows GDI+, une couleur est une valeur 32 bits avec 8 bits chacun pour alpha, rouge, vert et bleu.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Fusion alpha de lignes et de remplissages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864285"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="2c254-103">Fusion alpha de lignes et de remplissages</span><span class="sxs-lookup"><span data-stu-id="2c254-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="2c254-104">Dans Windows GDI+, une couleur est une valeur 32 bits avec 8 bits chacun pour alpha, rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="2c254-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="2c254-105">La valeur alpha indique la transparence de la couleur, c’est-à-dire l’étendue de la fusion de la couleur avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="2c254-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="2c254-106">Les valeurs alpha sont comprises entre 0 et 255, où 0 représente une couleur entièrement transparente et 255 représente une couleur entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="2c254-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="2c254-107">La fusion alpha est une fusion pixel par pixel des données de couleur d’arrière-plan et de la source.</span><span class="sxs-lookup"><span data-stu-id="2c254-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="2c254-108">Chacun des trois composants (rouge, vert, bleu) d’une couleur source donnée est fusionné avec le composant correspondant de la couleur d’arrière-plan en fonction de la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="2c254-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="2c254-109">displayColor = sourceColor × alpha/255 + backgroundColor × (255 – alpha)/255</span><span class="sxs-lookup"><span data-stu-id="2c254-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="2c254-110">Par exemple, supposons que le composant rouge de la couleur source est 150 et que le composant rouge de la couleur d’arrière-plan est 100.</span><span class="sxs-lookup"><span data-stu-id="2c254-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="2c254-111">Si la valeur alpha est 200, le composant rouge de la couleur résultante est calculé comme suit :</span><span class="sxs-lookup"><span data-stu-id="2c254-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="2c254-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="2c254-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="2c254-113">Les rubriques suivantes traitent de la fusion alpha plus en détail :</span><span class="sxs-lookup"><span data-stu-id="2c254-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="2c254-114">Dessin de lignes opaques et semi-transparentes</span><span class="sxs-lookup"><span data-stu-id="2c254-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="2c254-115">Dessiner avec des pinceaux opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="2c254-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="2c254-116">Utilisation du mode de composition pour contrôler la fusion alpha</span><span class="sxs-lookup"><span data-stu-id="2c254-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="2c254-117">Utilisation d’une matrice de couleurs pour définir des valeurs alpha dans des images</span><span class="sxs-lookup"><span data-stu-id="2c254-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="2c254-118">Définition des valeurs alpha de pixels individuels</span><span class="sxs-lookup"><span data-stu-id="2c254-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



