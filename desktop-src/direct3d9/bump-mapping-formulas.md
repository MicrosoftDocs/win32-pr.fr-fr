---
description: Direct3D applique les formules suivantes aux composants DU et DV dans chaque pixel de carte de relief.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formules de mappage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111663"
---
# <a name="bump-mapping-formulas-direct3d-9"></a><span data-ttu-id="a6962-103">Formules de mappage de relief (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a6962-103">Bump Mapping Formulas (Direct3D 9)</span></span>

<span data-ttu-id="a6962-104">Direct3D applique les formules suivantes aux composants D<sub>U</sub> et d<sub>V</sub> dans chaque pixel de carte de relief.</span><span class="sxs-lookup"><span data-stu-id="a6962-104">Direct3D applies the following formulas to the D<sub>U</sub> and D<sub>V</sub> components in each bump map pixel.</span></span>

![formules de transformations de matrice de mappage de relief](images/dudv-transform.png)

<span data-ttu-id="a6962-106">Dans ces formules, les variables D<sub>U</sub> et d<sub>V</sub> sont extraites directement d’un pixel de la carte de relief et transformées par une matrice 2x2 pour produire les valeurs Delta de sortie D<sub>U</sub>et d<sub>V</sub>.</span><span class="sxs-lookup"><span data-stu-id="a6962-106">In these formulas, the D<sub>U</sub> and D<sub>V</sub> variables are taken directly from a bump map pixel and transformed by a 2x2 matrix to produce the output delta values D<sub>U</sub>' and D<sub>V</sub>'.</span></span> <span data-ttu-id="a6962-107">Le système utilise les valeurs de sortie pour modifier les coordonnées de texture qui traitent la carte de l’environnement lors de la prochaine étape de texture.</span><span class="sxs-lookup"><span data-stu-id="a6962-107">The system uses the output values to modify the texture coordinates that address the environment map in the next texture stage.</span></span> <span data-ttu-id="a6962-108">Les coefficients de la matrice de transformation sont définis par l' \_ intermédiaire des États de texture D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 et D3DTSS BUMPENVMAT11 \_ .</span><span class="sxs-lookup"><span data-stu-id="a6962-108">The coefficients of the transformation matrix are set though the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT10, D3DTSS\_BUMPENVMAT01, and D3DTSS\_BUMPENVMAT11 texture stage states.</span></span>

<span data-ttu-id="a6962-109">En plus des valeurs Delta de v et v, le système peut calculer une valeur de luminance qu’il utilise pour moduler la couleur de la carte d’environnement lors de la phase de fusion suivante, comme illustré dans la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="a6962-109">In addition to the u and v delta values, the system can compute a luminance value that it uses to modulate the color of the environment map in the next blending stage, as shown in the following formula.</span></span>

![formule pour la luminance de sortie, calculée à partir du facteur d’échelle et du décalage](images/l-transform.png)

<span data-ttu-id="a6962-111">Dans cette formule, L’est la luminance de sortie calculée.</span><span class="sxs-lookup"><span data-stu-id="a6962-111">In this formula, L' is the output luminance being computed.</span></span> <span data-ttu-id="a6962-112">La variable L est la valeur de luminance tirée d’un pixel de la carte de relief, qui est multiplié par le facteur de mise à l’échelle, S et décalage par la valeur de la variable O. Les \_ États de texture D3DTSS BUMPENVLSCALE et D3DTSS \_ BUMPENVLOFFSET contrôlent les valeurs des variables s et O de la formule.</span><span class="sxs-lookup"><span data-stu-id="a6962-112">The L variable is the luminance value taken from a bump map pixel, which is multiplied by the scaling factor, S, and offset by the value in the variable O. The D3DTSS\_BUMPENVLSCALE and D3DTSS\_BUMPENVLOFFSET texture stage states control the values for the S and O variables in the formula.</span></span> <span data-ttu-id="a6962-113">Cette formule est appliquée uniquement lorsque l’opération de fusion de texture pour la phase qui contient la carte de relief est définie sur D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="a6962-113">This formula is only applied when the texture blending operation for the stage that contains the bump map is set to D3DTOP\_BUMPENVMAPLUMINANCE.</span></span> <span data-ttu-id="a6962-114">Lors de l’utilisation de D3DTOP \_ BUMPENVMAP, le système utilise la valeur 1,0 pour L'.</span><span class="sxs-lookup"><span data-stu-id="a6962-114">When using D3DTOP\_BUMPENVMAP, the system uses a value of 1.0 for L'.</span></span>

<span data-ttu-id="a6962-115">Après le calcul des valeurs Delta de sortie D<sub>U</sub>et d<sub>V</sub>', le système les ajoute aux coordonnées de texture à l’étape de texture suivante et module la couleur choisie par la luminance pour produire la couleur appliquée au polygone.</span><span class="sxs-lookup"><span data-stu-id="a6962-115">After computing the output delta values D<sub>U</sub>' and D<sub>V</sub>', the system adds them to the texture coordinates in the next texture stage, and modulates the chosen color by the luminance to produce the color applied to the polygon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6962-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a6962-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6962-117">Placage de relief</span><span class="sxs-lookup"><span data-stu-id="a6962-117">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



