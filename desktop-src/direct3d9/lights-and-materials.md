---
description: Les lumières sont utilisées pour illuminer les objets d’une scène.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Lumières et matériaux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f44a12c1be1e7a14f7bfe176d7f391901d2dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385532"
---
# <a name="lights-and-materials-direct3d-9"></a>Lumières et matériaux (Direct3D 9)

Les lumières sont utilisées pour illuminer les objets d’une scène. Lorsque l’éclairage est activé, Direct3D calcule la couleur de chaque vertex d’objet en fonction d’une combinaison de :

> [!Note]  
> Cette section concerne uniquement le pipeline à fonction fixe. Les nuanceurs programmables effectuent tous l’éclairage de manière explicite.

 

-   La couleur matérielle actuelle et les texels dans une carte de texture associée.
-   Couleurs diffuses et spéculaires au sommet, si elles sont spécifiées.
-   Couleur et intensité de la lumière produite par les sources de lumière dans la scène ou le niveau de lumière ambiante de la scène.

Lorsque vous utilisez l’éclairage et les matériaux Direct3D, vous autorisez Direct3D à gérer les détails de l’éclairage pour vous. Les utilisateurs avancés peuvent effectuer leurs propres éclairages, le cas échéant.

La façon dont vous travaillez avec l’éclairage et les matériaux fait une grande différence dans l’apparence de la scène rendue. Les matériaux définissent la façon dont la lumière reflète une surface. Les niveaux de lumière directe et de lumière ambiante définissent la lumière réfléchie. Vous devez utiliser des matériaux pour afficher une scène si l’éclairage est activé. Les lumières ne sont pas requises pour afficher une scène, mais les détails d’une scène rendue sans lumière ne sont pas visibles. Au mieux, le rendu d’une scène non éclairé entraîne la silhouette des objets dans la scène. Ce n’est pas assez détaillé dans la plupart des cas.

## <a name="direct-light-vs-ambient-light"></a>Lumière directe et lumière ambiante

Bien que les objets de lumière directe et ambiante illuminent les objets dans une scène, ils sont indépendants les uns des autres, ils ont des effets très différents et requièrent que vous les interagissez de manière totalement différente.

Direct Light est exactement ce qui suit : direct. Direct Light a toujours la direction et la couleur, et il s’agit d’un facteur pour les algorithmes d’ombrage, tels que l’ombrage Gouraud. Les différents types d’éclairage émettent une lumière directe de différentes façons, créant ainsi des effets d’atténuation spéciaux. Vous créez un ensemble de paramètres Light pour la lumière directe en appelant la méthode [**IDirect3DDevice9 :: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) .

La lumière ambiante est efficacement partout dans une scène. Vous pouvez le considérer comme un niveau général de lumière qui remplit une scène entière, quels que soient les objets et leurs emplacements dans cette scène. La lumière ambiante n’a pas de position ou de direction, uniquement la couleur et l’intensité. Chaque lumière vient s’ajouter à la lumière ambiante globale dans une scène. Définissez le niveau de lumière ambiante avec un appel à la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) , en spécifiant D3DRS \_ ambiant comme paramètre d' *État* et la couleur RVBA souhaitée comme paramètre de valeur.

La couleur de l’éclairage ambiant prend la forme d’une valeur RVBA, où chaque composant est une valeur entière comprise entre 0 et 255. Contrairement à la plupart des valeurs de couleur dans Direct3D.

Vous pouvez utiliser la macro [**D3DCOLOR \_ RVBA**](d3dcolor-rgba.md) pour générer des valeurs RVBA. Les composants rouge, vert et bleu se combinent pour créer la couleur finale de la lumière ambiante. Le composant alpha contrôle la transparence de la couleur. Lors de l’utilisation de l’accélération matérielle ou de l’émulation RGB, le composant alpha est ignoré.

## <a name="direct3d-light-model-vs-nature"></a>Modèle de lumière Direct3D et nature

Par nature, lorsque la lumière est émise à partir d’une source, elle est reflétée sur des centaines, voire des milliers ou des millions d’objets avant d’atteindre l’œil de l’utilisateur. À chaque fois qu’elle est reflétée, une lumière est absorbée par une surface, certaines d’entre elles sont dispersées dans des directions aléatoires, et le reste passe à une autre surface ou à l’oeil de l’utilisateur. Ce processus se poursuit jusqu’à ce que la lumière soit réduite à rien ou qu’un utilisateur perçoive la lumière.

Évidemment, les calculs nécessaires pour simuler parfaitement le comportement naturel de Light sont trop longs à utiliser pour les graphiques Direct3D en temps réel. Par conséquent, avec la vitesse à l’esprit, le modèle de lumière Direct3D se rapproche de la façon dont la lumière fonctionne dans le monde naturel. Direct3D décrit la lumière en termes de composants rouge, vert et bleu qui se combinent pour créer une couleur finale.

Dans Direct3D, lorsque la lumière reflète une surface, la couleur claire interagit de façon mathématique avec la surface elle-même pour créer la couleur finalement affichée à l’écran. Pour obtenir des informations spécifiques sur les algorithmes utilisés par Direct3D, voir [mathématique de l’éclairage (Direct3D 9)](mathematics-of-lighting.md).

Le modèle de lumière Direct3D généralise la lumière en deux types : la lumière ambiante et la lumière directe. Chacun a des attributs différents et chacun interagit avec les matériaux d’une surface de différentes façons. La lumière ambiante est de la lumière qui a été éparpillée tellement que la direction et la source sont indéterminées : elles maintiennent un faible niveau d’intensité partout. L’éclairage indirect utilisé par les photographes est un bon exemple de lumière ambiante. La lumière ambiante dans Direct3D, par nature, n’a pas de direction réelle ni de source, mais uniquement une couleur et une intensité. En fait, le niveau de lumière ambiante est complètement indépendant des objets d’une scène qui génèrent de la lumière. La lumière ambiante ne contribue pas à la réflexion spéculaire.

La lumière directe est la lumière générée par une source dans une scène. Il a toujours une couleur et une intensité, et il se déplace dans une direction spécifiée. La lumière directe interagit avec le matériau d’une surface pour créer des surbrillances spéculaires, et sa direction est utilisée comme facteur dans les algorithmes d’ombrage, y compris l’ombrage Gouraud. Quand la lumière directe est reflétée, elle ne contribue pas au niveau de la lumière ambiante dans une scène. Les sources d’une scène qui génèrent une lumière directe ont des caractéristiques différentes qui affectent la façon dont elles illuminent une scène.

En outre, le matériau d’un polygone a des propriétés qui affectent la façon dont ce polygone reflète la lumière qu’il reçoit. Vous définissez une caractéristique de réflexion unique qui décrit la façon dont la matière reflète la lumière ambiante et vous définissez des caractéristiques individuelles pour déterminer la réflectivité spéculaire et diffuse du matériau. Pour plus d’informations, consultez [Materials (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Valeurs de couleur pour les lumières et les matériaux

Direct3D décrit la couleur en termes de quatre composants (rouge, vert, bleu et alpha) qui combinent pour créer une couleur finale. La structure C++ [**D3DCOLORVALUE**](d3dcolorvalue.md) est définie pour contenir des valeurs pour chaque composant. Chaque membre est une valeur à virgule flottante qui est généralement comprise entre 0,0 et 1,0 inclus. Bien que les lumières et les matériaux utilisent la même structure pour décrire la couleur, les valeurs de la structure sont utilisées un peu différemment.

Les valeurs de couleur pour les sources lumineuses représentent la quantité d’un composant de lumière particulier qu’elle émet. Étant donné que les lumières n’utilisent pas de composant alpha, seuls les composants rouge, vert et bleu de la couleur sont pertinents. Vous pouvez visualiser les trois composants en tant que lentilles rouge, verte et bleue sur une télévision de projection. Chaque lentille peut être désactivée (une valeur 0,0 dans le membre approprié), elle peut être aussi brillante que possible (une valeur 1,0), ou il peut s’agir d’un niveau entre les deux. Les couleurs qui traversent les lentilles s’associent pour définir la couleur finale de la lumière. Une combinaison telle que R (1.0), G (1.0), B (1.0) crée une lumière blanche, où R (0.0), G (0.0), B (0.0) n’émet pas de lumière. Vous pouvez créer une lumière qui n’émet qu’un seul composant, ce qui donne une lumière de couleur rouge, verte ou bleue. ou la lumière peut utiliser des combinaisons pour émettre des couleurs comme le jaune ou le violet. Vous pouvez même définir des valeurs de composant de couleur négatives pour créer une « lumière sombre » qui supprime réellement la lumière d’une scène. Vous pouvez également définir les composants sur une valeur supérieure à 1,0 pour créer une lumière extrêmement brillante.

En revanche, avec les matériaux, les valeurs de couleur représentent la proportion d’un composant léger qui est reflétée par une surface rendue avec ce matériau. Un matériau dont les composants de couleur sont R (1.0), G (1.0), B (1.0), A (1.0) reflète tout le feu qui s’est produit. De même, un matériau avec R (0.0), G (1,0), B (0.0), A (1,0) reflète tout le feu vert qui lui est dirigé. Les matériaux ont plusieurs valeurs de réflectivité pour créer différents types d’effets.

Des informations supplémentaires sont contenues dans : [types de lumière (Direct3D 9)](light-types.md)et [Propriétés de lumière (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 
