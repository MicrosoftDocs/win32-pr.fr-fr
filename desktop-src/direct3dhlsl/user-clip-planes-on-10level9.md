---
title: Plans de clip utilisateur sur le matériel de niveau de fonctionnalité 9
description: À compter de Windows 8, le langage HLSL (High Level Shader Language) de Microsoft prend en charge une syntaxe que vous pouvez utiliser avec l’API Microsoft Direct3D 11 pour spécifier des plans de clip utilisateur sur le niveau de fonctionnalité 9 \_ x et plus.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315570"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Plans de clip utilisateur sur le matériel de niveau de fonctionnalité 9

À compter de Windows 8, le langage HLSL (High Level Shader Language) de Microsoft prend en charge une syntaxe que vous pouvez utiliser avec l’API Microsoft Direct3D 11 pour spécifier des plans de clip utilisateur sur le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et plus. Vous pouvez utiliser cette syntaxe pour écrire un nuanceur, puis utiliser cet objet de nuanceur avec l’API Direct3D 11 pour exécuter tous les niveaux de fonctionnalité Direct3D.

-   [Contexte](#background-reading)
-   [Syntaxe](#syntax)
-   [Création de plans de clip dans l’espace sur le niveau de fonctionnalité 9 et versions ultérieures](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Lecture en arrière-plan](#background-reading)
    -   [niveaux de fonctionnalité de 10Level9](#10level9-feature-levels)
    -   [Math plan de coupe](#clip-plane-math)
    -   [Découpage dans l’espace d’affichage](#clipping-in-view-space)
    -   [Matrice de projection](#projection-matrix)
    -   [Plan de découpage de l’espace](#clip-space-clip-plane)
-   [Rubriques connexes](#related-topics)

## <a name="background"></a>Arrière-plan

Vous pouvez accéder aux plans de clips utilisateur dans l’API Microsoft Direct3D 9 via les méthodes [**IDirect3DDevice9 :: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) et [**IDirect3DDevice9 :: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) . Dans Microsoft Direct3D 10 et versions ultérieures, vous pouvez accéder aux plans d’utilisateur à l’aide de la sémantique [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) . Mais avant Windows 8, SV \_ ClipDistance n’était pas disponible [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) pour \_ le matériel de niveau de fonctionnalité 9 x dans les API Direct3D 10 ou Direct3D 11. Donc, avant Windows 8, le seul moyen d’accéder aux plans de l’utilisateur avec le matériel de niveau de fonctionnalité 9 \_ x consistait à utiliser l’API Direct3D 9. Les applications Direct3D du Windows Store ne peuvent pas utiliser l’API Direct3D 9. Ici, nous décrivons la syntaxe que vous pouvez utiliser pour accéder aux plans de l’utilisateur via l’API Direct3D 11 au niveau de la fonctionnalité 9 \_ x et versions ultérieures.

Les applications utilisent des plans de coupe pour définir un ensemble de plans invisibles dans le monde 3D qui découpent (éliminent) toutes les primitives dessinées. Windows ne dessinera aucun pixel qui se trouve du côté négatif des plans de coupe. Les applications peuvent ensuite utiliser des plans de clip pour restituer les réflexions planaires.

## <a name="syntax"></a>Syntaxe

Utilisez cette syntaxe pour déclarer des plans d’éléments en tant qu’attributs de fonction dans une [déclaration de fonction](dx-graphics-hlsl-function-syntax.md). Par exemple, nous utilisons ici la syntaxe sur un fragment de nuanceur de sommets :

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

Cet exemple pour un fragment de nuanceur de sommets désigne deux plans de clip. Il montre que vous devez placer le nouvel attribut **clipplanes** entre crochets immédiatement avant la valeur de retour du nuanceur de sommets. Entre parenthèses après l’attribut **clipplanes** , vous fournissez une liste de 6 constantes **float4** au maximum qui définissent les coefficients de plan pour chaque plan de découpage actif. L’exemple montre également que vous devez faire en sorte que les coefficients de chaque plan résident dans une mémoire tampon constante.

> [!Note]  
> Aucune syntaxe n’est disponible pour désactiver dynamiquement un plan de découpage. Vous devez recompiler un nuanceur identique qui ne possède pas d’attribut **clipplanes** , ou votre application peut définir les coefficients dans votre mémoire tampon constante à zéro afin que le plan n’affecte plus aucune géométrie.

 

Cette syntaxe est disponible pour n’importe quelle cible de nuanceur de sommets 4,0 ou ultérieur, qui comprend vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 et vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Création de plans de clip dans l’espace sur le niveau de fonctionnalité 9 et versions ultérieures

Ici, nous montrons comment créer des plans de clips dans l’espace sur les [fonctionnalités](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et supérieures.

### <a name="background-reading"></a>Lecture en arrière-plan

« Introduction à la programmation de jeux en 3D avec DirectX 10 » de Frank D. Luna explique l’arrière-plan mathématique des graphiques (chapitres 1, 2 et 3) dont vous avez besoin, ainsi que les différentes transformations d’espaces et d’espaces qui se produisent dans le nuanceur de sommets (sections 5,6 et 5,8).

### <a name="10level9-feature-levels"></a>niveaux de fonctionnalité de 10Level9

Dans Direct3D 10 et versions ultérieures, vous pouvez découper n’importe quel espace logique, souvent dans l’espace universel ou dans l’espace d’affichage. Mais Direct3D 9 utilise l’espace de clip, qui est un espace de projection de préversion préalable. Les vecteurs sont dans l’espace de l’élément lorsque le nuanceur de sommets les passe aux étapes qui suivent dans le [pipeline Graphics](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).

Lorsque vous écrivez une application du Windows Store, vous devez utiliser les niveaux de fonctionnalité 10Level9 ([niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) pour que l’application puisse s’exécuter sur du matériel de niveau de fonctionnalité 9 \_ x et supérieur. Étant donné que votre application prend en charge le niveau de fonctionnalité 9 \_ x et les versions ultérieures, vous devez également utiliser la fonction d’application commune des plans de clip dans l’espace.

Quand vous compilez un nuanceur vertex avec vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 ou version ultérieure, ce nuanceur vertex peut utiliser l’attribut **clipplanes** . Un objet Direct3D 10 ou version ultérieure possède un produit scalaire du vertex émis qui contient chacune des constantes globales **float4** spécifiées dans l’attribut. L’objet Direct3D 9 a suffisamment de métadonnées pour obliger le runtime 10Level9 à émettre les appels appropriés à [**IDirect3DDevice9 :: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Math plan de coupe

Un plan de découpage est défini par un vecteur avec 4 composants. Les trois premiers composants définissent un vecteur x, y, z qui émane de l’origine de l’espace que vous souhaitez découper. Ce vecteur implique un plan, perpendiculaire au vecteur et s’exécutant par le biais de l’origine. Windows conserve tous les pixels du côté vecteur du plan et découpe tous les pixels situés derrière le plan. Le composant w est repousse le plan vers l’arrière et entraîne une réduction de la valeur de Windows (une w négative entraîne le découpage de Windows) le long de la ligne vectorielle. Si les composants x, y, z composent un vecteur unitaire (normalisé), w pousse les unités du plan w vers l’arrière.

La mathématique que l’unité de traitement graphique (GPU) effectue pour déterminer le découpage est un simple point entre le vecteur de vertex (x, y, z, 1) et le vecteur du plan de découpage. Cette opération mathématique crée une longueur de projection sur le vecteur de plan de découpage. Un point négatif indique que le vertex se trouve sur le côté coupé du plan.

### <a name="clipping-in-view-space"></a>Découpage dans l’espace d’affichage

Voici notre vertex dans l’espace d’affichage :

![vertex dans l’espace d’affichage](images/vertex-clip.png)

Voici notre plan de découpage dans l’espace d’affichage :

![plan de découpage dans l’espace d’affichage](images/clip-plane-view.png)

Voici le produit scalaire du vertex et du plan de découpage dans l’espace d’affichage :

ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>o</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  <sub></sub> c

Cette opération mathématique fonctionne pour un objet Direct3D 10 ou version ultérieure, mais ne fonctionne pas pour un objet Direct3D 9. Pour Direct3D 9, nous devons tout d’abord passer par notre transformation de projection dans l’espace.

### <a name="projection-matrix"></a>Matrice de projection

Une matrice de projection transforme un sommet de l’espace d’affichage (où l’origine est l’œil de la visionneuse, + x est à droite, + y est haut et + z est en avance) dans l’espace. La matrice de projection lit le vertex pour la capture de matériel et l' [étape de pixellisation](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage). Voici une matrice de perspective standard (les autres projections requièrent des maths différentes) :

<dl> taux *r*   de largeur/hauteur de fenêtre  
angle de visualisation de *α*    
distance *f*   de la visionneuse au plan lointain  
distance *n*   entre la visionneuse et le plan proche
</dl>![matrice de projection](images/projection-matrix.png)

La matrice suivante est une version simplifiée de la matrice précédente. Nous affichons la matrice de manière simplifiée afin de pouvoir l’utiliser ultérieurement dans l’opération de multiplication de matrice.

![matrice de projection simplifiée](images/projection-matrix2.png)

Nous transformons maintenant notre sommet d’espace d’affichage en espace de clip avec une matrice multiplier :

![multiplication de matrice](images/matrix-multiply.png)

Dans notre opération de multiplication de matrice, nos composants x et y sont légèrement ajustés, mais nos composants z et w sont très déformés. Notre plan de découpage ne nous donnera plus ce que nous voulons.

### <a name="clip-space-clip-plane"></a>Plan de découpage de l’espace

Ici, nous voulons créer un plan de clip d’espace disque dont le produit scalaire avec le sommet de l’espace disque nous donne la même valeur que **v · C** dans la section [découpage dans l’espace d’affichage](#clipping-in-view-space) .

![plan de découpage](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>o</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *c*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>P <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub></sub></sub>

À présent, nous pouvons diviser l’opération mathématique précédente par le composant vertex en quatre équations distinctes :

![composant de vertex x du produit de plan de découpage](images/clip-space-clip-plane-equ1.png)

![composant du vertex y du produit de plan de découpage](images/clip-space-clip-plane-equ2.png)

![composant de vertex w du produit de plan de découpage](images/clip-space-clip-plane-equ3.png)

![composant de sommet z du produit de plan de découpage](images/clip-space-clip-plane-equ4.png)

Notre plan de découpage d’espace de vue et notre matrice de projection dérivent et nous donnent notre plan de clip d’espace.

![plan de découpage de l’espace](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Syntaxe de la déclaration des fonctions](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 