---
description: De nombreuses techniques de rendu et de génération de contenu requièrent une carte unique et sans chevauchement d’un signal 2D (par exemple, une texture) sur une maille.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Utilisation de UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104211151"
---
# <a name="using-uvatlas-direct3d-9"></a>Utilisation de UVAtlas (Direct3D 9)

De nombreuses techniques de rendu et de génération de contenu requièrent une carte unique et sans chevauchement d’un signal 2D (par exemple, une texture) sur une maille. Ces techniques sont les suivantes :

-   Mappage normal/de déplacement
-   Simulations d’espace de textures PRT et cartes de lumière
-   Peinture de surface
-   Éclairage de l’espace de texture

La génération manuelle d’un mappage UV unique est souvent longue et fastidieuse. Cela est particulièrement vrai lorsque la géométrie d’entrée est complexe et efficace/à faible distorsion-l’utilisation de l’espace est souhaitée. L’illustration suivante montre un exemple de maillage et son Atlas de texture correspondant.

![Affiche un exemple de maillage et son Atlas de texture correspondant.](images/uvatlas1.jpg)

Cet exemple montre un maillage (à gauche) et la carte normale d’espace UV correspondante (à droite). Notez que l’Atlas de textures contient plusieurs groupes ou clusters de données ; chaque cluster est appelé un graphique et, dans l’exemple ci-dessus, l’affichage contient les données normales d’une partie de la maille.

Les API D3DX UVAtlas génèrent automatiquement un Atlas de texture optimal et sans chevauchement. Les API fournissent des paramètres d’entrée qui vous permettent d’effectuer les opérations suivantes :

-   Réduire l’étirement, la distorsion et le sous-échantillonnage de texture.
-   Agrandissez la densité de compression de l’espace de texture pour une utilisation efficace de la mémoire.
-   Fournissez un échantillonnage pair sur la maille, en minimisant les discontinuités de la fréquence d’échantillonnage.

## <a name="how-uvatlas-works"></a>Fonctionnement de UVAtlas

Les API UVAtlas (voir [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) génèrent un Atlas de texture en partitionnant une surface en graphiques et en compaquetant les graphiques dans un Atlas de texture. Utilisez [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) et [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) pour effectuer ces étapes séparément. ou utilisez [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) pour partitionner, paramétrer et compresser en un seul appel.

-   [Partitionnement et paramétrage d’une maille](#partitioning-and-parameterizing-a-mesh)
-   [Utilisation de dizaines de mesures intégrés pour contrôler le paramétrage](#using-integrated-metric-tensors-to-control-parameterization)
-   [Utilisation des données d’adjacence pour les froissures spécifiés par l’utilisateur](#using-adjacency-data-for-user-specified-creases)
-   [Empaqueter des graphiques dans un Atlas](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a>Partitionnement et paramétrage d’une maille

Tout d’abord, le maillage est partitionné en graphiques, puis chaque graphique est paramétré dans son propre \[ \] espace UV. Un cylindre peut être paramétré par un graphique ; en revanche, une sphère nécessitera deux graphiques, comme indiqué dans l’illustration suivante.

![illustration d’une sphère partitionnée en deux graphiques](images/uvatlas3.jpg)

Une maille qui peut être paramétrée avec un seul graphique est classée en tant que « homeomorphic sur un disque », ce qui signifie que vous pouvez répartir un disque flexible et extensible à l’infini sur le graphique et couvrir parfaitement la géométrie. Cet étirement, appelé homeomorphism, est une fonction bidirectionnelle. Cela signifie que vous pouvez passer d’un paramétrage à l’autre sans perdre d’informations.

Très peu de maillages réels peuvent être paramétrés en deux dimensions sans les séparer en clusters ou en graphiques. L’illustration suivante montre un autre exemple de maillage et son Atlas de textures correspondant.

![Montre un exemple de maillage avec différentes formes et l’Atlas de texture correspondant.](images/uvatlas2.jpg)

Il existe deux paramètres qui déterminent le nombre de graphiques créés :

-   Nombre maximal de graphiques autorisés pour l’Atlas
-   Quantité maximale d’étirement autorisée pour chaque graphique

La quantité d’étirement détermine le nombre de graphiques qui sont générés et la qualité globale de l’échantillonnage. Les étendues Stretch sont comprises entre 0,0 (sans Stretch) et 1,0 (n’importe quelle quantité d’étirement). D3DXUVAtlasCreate et D3DXUVAtlasPartition retournent l’Stretch maximal généré par l’algorithme. L’illustration suivante montre un autre exemple de maillage et son Atlas de textures correspondant.

![illustration d’un exemple de maillage et de l’Atlas de texture correspondant](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a>Utilisation de dizaines de mesures intégrés pour contrôler le paramétrage

La hiérarchisation de l’espace de texture peut être spécifiée pour chaque triangle. Des dizaines de métriques intégrés peuvent être fournis pour contrôler la façon dont les triangles sont étirés dans l’Atlas d’espace de texture qui en résulte. Les IMT peuvent être spécifiés directement ou calculés en fonction d’un signal d’entrée à l’aide des fonctions de calcul D3DX IMT. Une métrique intégrée tenseur (ou IMT) est une matrice 2x2 2x2 qui décrit comment un triangle est étiré dans l’Atlas. Chaque IMT est défini par 3 valeurs float, appelées (a, b, c). Elles peuvent être réorganisées dans une matrice 2x2 symétrique comme suit :


```
a b
b c
```



Le IMT peut ensuite être utilisé pour déterminer la distance entre deux vecteurs. À partir de deux vecteurs v1 et v2, où :


```
vector v1
vector v2 = v1 + (s,t)
```



La distance entre v1 et V2 peut être calculée comme suit :


```
sqrt((s, t) * M * (s, t)^T)
```



En d’autres termes, le vecteur (s, t) peut être la grandeur de l’étirement dans une direction arbitraire dans l’espace u-v. Dans ce cas, le vecteur s est une direction entre le premier et le deuxième vertex, et t est le produit croisé de la normale et du s. Exemple :


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



Les IMT peuvent être spécifiés directement ou calculés en fonction d’un signal d’entrée à l’aide des fonctions de calcul D3DX IMT : D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal et D3DXComputeIMTFromTexture \_ Graphics.

Spécifiez les données IMT directement si vous souhaitez contrôler la façon dont l’espace de texture est alloué à des triangles individuels. En procédant ainsi, allouez plus d’espace dans l’Atlas à des zones importantes d’une maille (comme le visage d’un personnage ou le logo du coffre, ou les régions d’une scène près du parcours de marche d’un joueur). En spécifiant des IMT qui sont des multiples de la matrice d’identité, les triangles résultants sont mis à l’échelle uniformément dans l’espace de texture.

Par exemple, à partir d’une carte normale haute résolution, vous pouvez calculer IMT pour fournir plus d’espace de texture aux zones de signal de fréquence supérieure dans la carte normale. Les triangles qui sont « plats » (qui sont mappés à des régions constantes de la carte normale d’origine) recevront moins d’espace de texture. Les triangles qui contiennent un grand nombre de détails de la carte normale reçoivent plus de zone de texture dans le résultat final. Vous pouvez ensuite rééchantillonner la carte normale en une texture plus petite tout en conservant les détails, ou vous pouvez recalculer la carte normale avec le mappage UV optimal.

### <a name="using-adjacency-data-for-user-specified-creases"></a>Utilisation des données d’adjacence pour les froissures spécifiés par l’utilisateur

Les informations d’adjacence définies par l’utilisateur peuvent être fournies à la fonction de partitionnement pour décrire des froissures prédéfinis dans la maille, et ainsi définir une limite de graphique entre des visages adjacents. C’est un moyen simple pour l’appelant de spécifier son propre partitionnement de graphique comme entrée dans l’algorithme, ce qui permet d’affiner davantage les graphiques pour que l’étirement soit inférieur au maximum autorisé.

### <a name="example"></a>Exemple

Cet exemple montre comment vous pouvez utiliser les API UVAtlas et la visionneuse DirectX (Dxviewer.exe) pour rechercher et corriger les discontinuités dans votre modèle qui peuvent affecter considérablement la taille de votre Atlas de texture. Vous pouvez obtenir Dxviewer.exe et en savoir plus à ce sujet à partir du kit de développement logiciel (SDK) DirectX. Dxviewer.exe a été supprimé du kit de développement logiciel (SDK) DirectX après la version du 2009 août afin de l’afficher, vous aurez besoin d’au moins le kit de développement logiciel (SDK) DirectX du 2009 août. Pour plus d’informations sur DirectX SDK, consultez [où se trouve le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md).

Supposons que vous avez commencé avec un modèle dans votre logiciel de génération de contenu préféré (cet exemple utilise un modèle de tête de nain créé dans Maya). Exportez le modèle texturé dans un fichier. x et créez un Atlas de texture avec D3DXUVAtlasCreate. L’Atlas de texture qui en résulte ressemble à l’illustration suivante.

![illustration d’un modèle d’Atlas pour un nain](images/uvatlas5.jpg)

L’Atlas a 22 graphiques et une extension maximale de 0,994.

Examinez maintenant le modèle texturé pour voir comment l’Atlas de texture est mappé à la géométrie. Pour ce faire, chargez le modèle dans l’outil visionneuse :

-   Ouvrez l’outil visionneuse à partir des utilitaires DirectX.
-   Chargez le fichier. x en cliquant sur le bouton Ouvrir.
-   Activation de l’option d’affichage froissures en cliquant sur le bouton afficher et en sélectionnant froissures dans le menu contextuel.

L’illustration suivante montre ce que vous devez voir dans l’outil visionneuse.

![illustration d’une maille texturée dans l’outil visionneuse](images/uvatlas6c.jpg)

Chaque ligne est un pli qui est un bord adjacent entre deux graphiques dans l’Atlas de textures. Le nombre de graphiques générés par l’algorithme est dû à de légères différences, peut-être en raison de discontinuités dans les normales. Ces petites différences peuvent être réduites en soudant des données, c’est-à-dire en forçant les données qui sont pratiquement égales à. Pour souder les normales et les skinweights :

-   Exécutez l’outil DirectX OPS (dxops.exe) avec la ligne de commande suivante sur la maille (en remplaçant « modelName. x » par le nom de votre modèle) :
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

Cela permet de comparer les normales et les skinweights, et où ils diffèrent de la valeur par moins de 2,01, les données sont égales. Les illustrations suivantes montrent un maximum d’œil pour voir les froissures avant le soudage (à gauche) et les froissures après soudure (à droite) :

![illustration des froissures avant le soudage](images/uvatlas6a.jpg)![illustration des froissures après soudure](images/uvatlas6b.jpg)

Figure 7 : suppression des froissures par soudure

Dans cet exemple, la soudure a retiré 86 sommets du maillage d’entrée. Avec moins de froissures dans la maille, vous pouvez régénérer l’Atlas, comme le montre l’illustration suivante.

![illustration du nouvel Atlas avec les froissures supprimés](images/uvatlas8.jpg)

L’Atlas n’a que 7 graphiques et une valeur maximale de 0,0776 environ. Le nouvel Atlas s’intègre désormais à une texture plus petite (environ 30% de plus petite taille dans cet exemple).

### <a name="packing-charts-into-an-atlas"></a>Empaqueter des graphiques dans un Atlas

Une fois qu’un maillage a été partitionné en graphiques paramétrés individuellement, les graphiques doivent être compactés efficacement dans une seule carte de texture. Il s’agit de la deuxième étape de D3DXUVAtlasCreate ou peut être appelée explicitement en appelant D3DXUVAtlasPack.

Les graphiques compactés sont séparés par une largeur de reliure spécifiée par l’utilisateur. La largeur de la reliure correspond à la quantité de séparation entre les graphiques et permet l’interpolation bilinéaire et le mappage MIP pour éviter le rendu des artefacts aux limites du graphique. D3DX fournit une interface pour remplir automatiquement ces gouttières. pour plus d’informations, consultez [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

## <a name="integrating-uvatlas-into-your-pipeline"></a>Intégration de UVAtlas dans votre pipeline

En plus d’être appelé par l’artiste avant la peinture de texture, ces fonctions peuvent être intégrées dans un pipeline d’art automatisé. Par exemple, un appel UVAtlas peut être émis automatiquement après la mise à jour d’un élément multimédia, avant d’effectuer une simulation PRT ou un test de mappage normal. Cela évite de devoir réparer manuellement manuellement le mappage UV d’un objet si la topologie du maillage a été modifiée.

Pour obtenir des exemples d’utilisation des fonctions UVAtlas, consultez l' [outil Command-Line de l’Atlas UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> </dl>

 

 
