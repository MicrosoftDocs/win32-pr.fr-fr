---
description: Direct3D applique les formules suivantes aux composants DU et DV dans chaque pixel de carte de relief.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formules de mappage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035a28966c841f7d593cb46c7c7d969f7b2addaacb6cf43e25ceebdca83ff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805852"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Formules de mappage de relief (Direct3D 9)

Direct3D applique les formules suivantes aux composants D<sub>U</sub> et d<sub>V</sub> dans chaque pixel de carte de relief.

![formules de transformations de matrice de mappage de relief](images/dudv-transform.png)

Dans ces formules, les variables D<sub>U</sub> et d<sub>V</sub> sont extraites directement d’un pixel de la carte de relief et transformées par une matrice 2x2 pour produire les valeurs Delta de sortie D<sub>U</sub>et d<sub>V</sub>. Le système utilise les valeurs de sortie pour modifier les coordonnées de texture qui traitent la carte de l’environnement lors de la prochaine étape de texture. Les coefficients de la matrice de transformation sont définis par l' \_ intermédiaire des États de texture D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 et D3DTSS BUMPENVMAT11 \_ .

En plus des valeurs Delta de v et v, le système peut calculer une valeur de luminance qu’il utilise pour moduler la couleur de la carte d’environnement lors de la phase de fusion suivante, comme illustré dans la formule suivante.

![formule pour la luminance de sortie, calculée à partir du facteur d’échelle et du décalage](images/l-transform.png)

Dans cette formule, L’est la luminance de sortie calculée. La variable L est la valeur de luminance tirée d’un pixel de la carte de relief, qui est multiplié par le facteur de mise à l’échelle, S et décalage par la valeur de la variable O. Les \_ États de texture D3DTSS BUMPENVLSCALE et D3DTSS \_ BUMPENVLOFFSET contrôlent les valeurs des variables s et O de la formule. Cette formule est appliquée uniquement lorsque l’opération de fusion de texture pour la phase qui contient la carte de relief est définie sur D3DTOP \_ BUMPENVMAPLUMINANCE. Lors de l’utilisation de D3DTOP \_ BUMPENVMAP, le système utilise la valeur 1,0 pour L'.

Après le calcul des valeurs Delta de sortie D<sub>U</sub>et d<sub>V</sub>', le système les ajoute aux coordonnées de texture à l’étape de texture suivante et module la couleur choisie par la luminance pour produire la couleur appliquée au polygone.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de relief](bump-mapping.md)
</dt> </dl>

 

 



