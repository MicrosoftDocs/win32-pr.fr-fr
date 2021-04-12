---
description: La partie de Direct3D qui pousse la géométrie via le pipeline de géométrie de fonction fixe est le moteur de transformation.
ms.assetid: ed52e32f-8fae-4e6f-b908-26e05ce940cc
title: Transformations (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482ef12c88140c2eff4c61e634fd3297aeaf295
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392880"
---
# <a name="transforms-direct3d-9"></a>Transformations (Direct3D 9)

La partie de Direct3D qui pousse la géométrie via le pipeline de géométrie de fonction fixe est le moteur de transformation. Il localise le modèle et la visionneuse dans le monde entier, projette les sommets pour l’affichage à l’écran et découpe les sommets dans la fenêtre d’affichage. Le moteur de transformation effectue également des calculs d’éclairage pour déterminer les composants diffus et spéculaire à chaque vertex.

Le pipeline Geometry prend des sommets comme entrée. Le moteur de transformation applique les transformations universelles, de vue et de projection aux sommets, découpe le résultat et transmet tout le contenu au rastériseur.

Au début du pipeline, les vertex d’un modèle sont déclarés par rapport à un système de coordonnées local. Il s’agit d’une origine locale et d’une orientation. Cette orientation des coordonnées est souvent appelée espace de modèle, et les coordonnées individuelles sont appelées coordonnées de modèle.

La première étape du pipeline de géométrie transforme les vertex d’un modèle de leur système de coordonnées local en un système de coordonnées utilisé par tous les objets d’une scène. Le processus de réorientation des vertex est appelé la transformation universelle. Cette nouvelle orientation est communément appelée espace universel, et chaque vertex dans l’espace universel est déclaré à l’aide de coordonnées universelles.

À l’étape suivante, les vertex qui décrivent votre monde 3D sont orientés par rapport à une caméra. Autrement dit, votre application choisit un point de vue pour la scène, et les coordonnées de l’espace universel sont déplacées et pivotées autour de la vue de l’appareil photo, ce qui fait de l’espace universel dans l’espace de l’appareil photo. Il s’agit de la transformation de la vue.

L’étape suivante est la transformation de projection. Dans cette partie du pipeline, les objets sont généralement mis à l’échelle en fonction de leur distance par rapport à la visionneuse afin de fournir l’illusion de profondeur à une scène. les objets proches sont rendus plus volumineux que les objets distants, et ainsi de suite. Par souci de simplicité, cette documentation fait référence à l’espace dans lequel les vertex existent après la transformation de projection en tant qu’espace de projection. Certains livres graphiques peuvent faire référence à l’espace de projection comme un espace homogène après la perspective. Toutes les transformations de projection n’ajustent pas la taille des objets dans une scène. Une projection telle que celle-ci est parfois appelée projection affine ou orthogonale.

Dans la dernière partie du pipeline, tous les vertex qui ne seront pas visibles à l’écran sont supprimés, de sorte que le rastériseur ne prend pas le temps de calculer les couleurs et l’ombrage pour un élément qui ne sera jamais visible. Ce processus est appelé découpage. Après le découpage, les sommets restants sont mis à l’échelle en fonction des paramètres de la fenêtre d’affichage et convertis en coordonnées d’écran. Les vertex résultants, visibles à l’écran lorsque la scène est pixellisée, existent dans l’espace à l’écran.

Les transformations sont utilisées pour convertir la géométrie d’un objet d’un espace de coordonnées à un autre. Direct3D utilise des matrices pour effectuer des transformations 3D. Cette section explique comment les matrices créent des transformations 3D, décrit certaines utilisations courantes des transformations et détaille la façon dont vous pouvez combiner des matrices pour produire une matrice unique qui englobe plusieurs transformations.

-   [Transformation universelle (Direct3D 9)](world-transform.md) : conversion de l’espace de modèle en espace universel
-   [Vue de la transformation (Direct3D 9)](view-transform.md) -conversion à partir de l’espace universel pour afficher l’espace
-   [Transformation de projection (Direct3D 9)](projection-transform.md) -conversion de l’espace d’affichage à l’espace de projection

## <a name="matrix-transforms"></a>Transformations de matrice

Dans les applications qui fonctionnent avec des graphiques 3D, vous pouvez utiliser les transformations géométriques pour effectuer les opérations suivantes :

-   Exprimer l’emplacement d’un objet par rapport à un autre objet.
-   Faire pivoter et dimensionner les objets.
-   Modifiez les positions, les directions et les perspectives d’affichage.

Vous pouvez transformer n’importe quel point (x, y, z) en un autre point (x, y, z) à l’aide d’une matrice 4x4, comme illustré dans l’équation suivante.

![équation de la transformation de tout point en un autre point](images/matmult.png)

Effectuez les équations suivantes sur (x, y, z) et la matrice pour produire le point (x, y, z).

![équations pour le nouveau point](images/matexpnd.png)

Les transformations les plus courantes sont la traduction, la rotation et la mise à l’échelle. Vous pouvez combiner les matrices qui produisent ces effets dans une seule matrice pour calculer plusieurs transformations à la fois. Par exemple, vous pouvez créer une matrice unique pour traduire et faire pivoter une série de points.

Les matrices sont écrites dans l’ordre des colonnes de lignes. Une matrice qui ajuste uniformément les sommets le long de chaque axe, appelée mise à l’échelle uniforme, est représentée par la matrice suivante à l’aide de la notation mathématique.

![équation d’une matrice pour la mise à l’échelle uniforme](images/matrix.png)

En C++, Direct3D déclare des matrices sous la forme d’un tableau à deux dimensions, à l’aide de la structure [**D3DMATRIX**](d3dmatrix.md) . L’exemple suivant montre comment initialiser une structure **D3DMATRIX** pour qu’elle agisse comme une matrice de mise à l’échelle uniforme.


```
// In this example, s is a variable of type float.

D3DMATRIX scale = {
    s,               0.0f,            0.0f,            0.0f,
    0.0f,            s,               0.0f,            0.0f,
    0.0f,            0.0f,            s,               0.0f,
    0.0f,            0.0f,            0.0f,            1.0f
};
```



## <a name="translate"></a>Translate

L’équation suivante traduit le point (x, y, z) en un nouveau point (x, y, z).

![équation d’une matrice de translation pour un nouveau point](images/transl8.png)

Vous pouvez créer manuellement une matrice de traduction en C++. L’exemple suivant montre le code source d’une fonction qui crée une matrice pour traduire des vertex.


```
D3DXMATRIX Translate(const float dx, const float dy, const float dz) {
    D3DXMATRIX ret;

    D3DXMatrixIdentity(&ret);
    ret(3, 0) = dx;
    ret(3, 1) = dy;
    ret(3, 2) = dz;
    return ret;
}    // End of Translate
```



Pour plus de commodité, la bibliothèque de l’utilitaire D3DX fournit la fonction [**D3DXMatrixTranslation**](d3dxmatrixtranslation.md) .

## <a name="scale"></a>Scale

L’équation suivante met à l’échelle le point (x, y, z) en valeurs arbitraires dans les directions x, y et z vers un nouveau point (x, y, z).

![équation d’une matrice de mise à l’échelle pour un nouveau point](images/matscale.png)

## <a name="rotate"></a>Faire pivoter

Les transformations décrites ici sont destinées aux systèmes de coordonnées de gauche et peuvent être différentes des matrices de transformation que vous avez vues ailleurs.

L’équation suivante fait pivoter le point (x, y, z) autour de l’axe x, produisant un nouveau point (x, y, z).

![équation d’une matrice de rotation x pour un nouveau point](images/matxrot.png)

L’équation suivante fait pivoter le point autour de l’axe y.

![équation d’une matrice de rotation y pour un nouveau point](images/matyrot.png)

L’équation suivante fait pivoter le point autour de l’axe z.

![équation d’une matrice de rotation z pour un nouveau point](images/matzrot.png)

Dans ces exemples de matrices, la lettre grecque thêta représente l’angle de rotation, en radians. Les angles sont mesurés dans le sens des aiguilles d’une montre sur l’axe de rotation vers l’origine.

Dans une application C++, utilisez les fonctions [**D3DXMatrixRotationX**](d3dxmatrixrotationx.md), [**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)et [**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md) fournies par la bibliothèque de l’utilitaire D3DX pour créer des matrices de rotation. Voici le code de la fonction **D3DXMatrixRotationX** .


```
D3DXMATRIX* WINAPI D3DXMatrixRotationX
    ( D3DXMATRIX *pOut, float angle )
{
#if DBG
    if(!pOut)
        return NULL;
#endif

    float sin, cos;
    sincosf(angle, &sin, &cos);  // Determine sin and cos of angle

    pOut->_11 = 1.0f; pOut->_12 =  0.0f;   pOut->_13 = 0.0f; pOut->_14 = 0.0f;
    pOut->_21 = 0.0f; pOut->_22 =  cos;    pOut->_23 = sin;  pOut->_24 = 0.0f;
    pOut->_31 = 0.0f; pOut->_32 = -sin;    pOut->_33 = cos;  pOut->_34 = 0.0f;
    pOut->_41 = 0.0f; pOut->_42 =  0.0f;   pOut->_43 = 0.0f; pOut->_44 = 1.0f;

    return pOut;
}
```



## <a name="concatenating-matrices"></a>Concaténation de matrices

L’un des avantages de l’utilisation des matrices est que vous pouvez combiner les effets de deux matrices ou plus en les multipliant. Cela signifie que, pour faire pivoter un modèle, puis le traduire à un emplacement donné, vous n’avez pas besoin d’appliquer deux matrices. Au lieu de cela, vous multipliez les matrices de rotation et de translation pour produire une matrice composite qui contient tous les effets. Ce processus, appelé concaténation de matrice, peut être écrit avec l’équation suivante.

![équation de la concaténation de matrice](images/matrxcat.png)

Dans cette équation, C est la matrice composite en cours de création et M ₁ à mn sont les matrices individuelles. Dans la plupart des cas, seules deux ou trois matrices sont concaténées, mais il n’existe aucune limite.

Utilisez la fonction [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) pour effectuer une multiplication de matrice.

L’ordre dans lequel la multiplication de la matrice est effectuée est essentiel. La formule précédente reflète la règle de la concaténation de matrice de gauche à droite. Autrement dit, les effets visibles des matrices que vous utilisez pour créer une matrice composite se produisent dans l’ordre de gauche à droite. L’exemple suivant illustre une matrice universelle classique. Imaginez que vous créez la matrice universelle pour un soubattante volante de stéréotype. Vous souhaiterez probablement faire tourner le volant volant autour de son centre-l’axe y de l’espace de modèle, et le traduire à un autre emplacement de votre scène. Pour obtenir cet effet, vous créez d’abord une matrice de rotation, puis vous la multipliez par une matrice de traduction, comme illustré dans l’équation suivante.

![équation de spin basée sur une matrice de rotation et une matrice de traduction](images/wrldexpl.png)

Dans cette formule, R<sub>y</sub> est une matrice de rotation autour de l’axe des y et T<sub>w</sub> est une translation à une position en coordonnées universelles.

L’ordre dans lequel vous multipliez les matrices est important car, contrairement à la multiplication de deux valeurs scalaires, la multiplication de matrices n’est pas commutative. La multiplication des matrices dans l’ordre opposé a pour effet visuel de traduire le volant volant en position d’espace universel, puis de le faire pivoter autour de l’origine du monde.

Quel que soit le type de matrice que vous créez, n’oubliez pas la règle de gauche à droite pour vous assurer que vous atteignez les effets attendus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 



