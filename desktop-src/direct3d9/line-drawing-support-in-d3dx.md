---
description: D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Prise en charge des dessins en ligne dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a0fdeb24dad1107f85e6c79603368776bce15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392691"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Prise en charge des dessins en ligne dans D3DX (Direct3D 9)

D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.

D3DX prend en charge les lignes avec anticrénelage à l’étendue d’un pixel. Les modèles de ligne ne sont plus pris en charge.

La bibliothèque de dessins en ligne émule les lignes à l’aide de triangles de texture et suppose ce qui suit :

-   Le matériel est disponible via les interfaces Direct3D 9.
-   Au moins une étape de texture est disponible.
-   les textures 64x64 sont utilisées.
-   Les modes suivants sont disponibles :
    -   Filtrage bilinéaire
    -   Mode d’adresse de serrage
    -   Mode d’adresse de retour à la ligne
    -   Module alpha op modulation
    -   Fusion alpha (SRCBLEND = SRC \_ alpha, DESTBLEND = INV \_ src \_ alpha)
    -   Test alpha si la fusion alpha n’est pas disponible ; résultat de qualité inférieure

Pour le rendu de ligne avec anticrénelage dans les cibles de rendu à échantillonnages, utilisez [**ID3DXLine**](id3dxline.md) qui génère des polygones texturés. Les valeurs de couverture des pixels, générées par la pixellisation de ligne avec anticrénelage, modulent la valeur alpha du pixel calculée par le nuanceur de pixels. Pour dessiner une ligne avec anticrénelage, une application doit activer la fusion alpha, puis elle doit définir l' \_ État de rendu D3DRS ANTIALIASEDLINEENABLE sur **true**.

## <a name="functionality-description"></a>Description de la fonctionnalité

La bibliothèque prend en charge le dessin des bandes de couleur avec les caractéristiques de ligne suivantes, chacune d’elles étant indépendante des autres :

-   Largeur de ligne
-   Modèle de ligne avec répétition (le compteur de modèle de ligne réinitialise avec chaque [**ID3DXLine ::D RAW**](id3dxline--draw.md) ou [**ID3DXLine ::D rawtransform**](id3dxline--drawtransform.md) . Elle n’est pas réinitialisée avec chaque segment de la bande.
-   Anticrénelage
-   Lignes de style OpenGL

> [!Note]  
> Aucune Mitre n’est prise en charge.

 

La bibliothèque utilise la prise en charge de dessin de ligne matérielle native (si disponible dans l’appareil) uniquement si :

-   La largeur de ligne est 1.
-   Aucun modèle de ligne n’est activé.

Les lignes avec anticrénelage à l’ensemble des pixels sont prises en charge par un matériel, de sorte que la bibliothèque utilise cette, si elle est disponible. Le membre LineCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) énumère les fonctionnalités matérielles pour les primitives de dessin de lignes.

Lorsque le dessin en ligne de logiciel est utilisé, chaque ligne est développée dans un rectangle et quatre sommets sont envoyés au pilote.

Chaque segment de ligne est dessiné à l’aide de deux triangles. La largeur de la primitive est la largeur spécifiée plus 1,0, ce qui peut entraîner une ligne ou une colonne supplémentaire de pixels. À mesure que la ligne est plus grande, le dégradé d’antialias dans la texture devient plus grossiste et plus les texels entièrement opaques sont répliqués au milieu. Le dégradé est encodé dans l’axe v de la texture, et est généralement répliqué le long de la direction u. Le mode d’adressage de la texture pour v est clamp.

Chaque segment de ligne de la liste peut être considéré comme une ligne distincte qui commence à partir du point de terminaison précédent.

La qualité de l’anticrénelage le long des bords parallèles à la longueur de la ligne d’origine souffre de l’épaisseur de la ligne. Il est prévu que les largeurs de ligne supérieures à 32,0 commencent à présenter des artefacts le long de ces bords.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



