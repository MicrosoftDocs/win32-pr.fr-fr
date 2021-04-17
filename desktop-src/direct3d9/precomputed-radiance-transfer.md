---
description: Transfert de luminance précalculé (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transfert de luminance précalculé (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553346"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Transfert de luminance précalculé (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Utilisation du transfert de luminance précalculé

Il existe plusieurs formes de complexité dans des scènes intéressantes, notamment la façon dont l’environnement d’éclairage est modélisé (autrement dit, les modèles d’éclairage de zone par rapport aux points/directionnels) et le type d’effets globaux modélisés (par exemple, les ombres, les interreflets, la diffusion sous-surface). Les techniques de rendu interactives traditionnelles modélisent une quantité limitée de cette complexité. PRT active ces effets avec des restrictions significatives :

-   Les objets sont supposés être rigides (c’est-à-dire, aucune déformations).
-   Il s’agit d’une approche centrée sur les objets (à moins que les objets ne soient déplacés ensemble, ces effets globaux ne sont pas maintenus entre eux).
-   Seule l’éclairage à basse fréquence est modélisé (ce qui entraîne des ombres douces). Pour les lumières haute fréquence (ombres nettes), les techniques traditionnelles devraient être utilisées.

PRT requiert l’un des éléments suivants, mais pas les deux :

-   modèles hautement fractionnés et vs \_ 1 \_ 1
-   PS \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Éclairage diffus standard par rapport à PRT

L’illustration suivante est rendue à l’aide du modèle d’éclairage traditionnel (n · l). Les ombres nettes peuvent être activées à l’aide d’une autre méthode de mise en Shadow et d’une certaine forme de technique d’occultation (cartes de profondeur des tons foncés ou volumes L’ajout de plusieurs lumières nécessiterait soit plusieurs passes (si des ombres doivent être utilisées), soit des nuanceurs plus complexes avec des techniques traditionnelles.

![capture d’écran d’une illustration rendue à l’aide du modèle d’éclairage traditionnel](images/prt-diffuse-cropped.png)

L’illustration suivante est rendue avec PRT à l’aide de la meilleure approximation d’une lumière directionnelle unique qu’il peut résoudre. Il en résulte des ombres douces qui seraient difficiles à produire avec les techniques traditionnelles. Étant donné que PRT modélise toujours des environnements d’éclairage complets en ajoutant plusieurs lumières ou en utilisant une carte d’environnement, vous modifiez uniquement les valeurs (mais pas le nombre) des constantes utilisées par le nuanceur.

![capture d’écran d’une illustration rendue à l’aide de PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT avec interreflets

L’éclairage direct atteint la surface directement à partir de la lumière. Les interreflets ont une lumière qui atteint la surface après avoir rebondissant une autre surface un certain nombre de fois. PRT peut modéliser ce comportement sans modifier les performances au moment de l’exécution en exécutant simplement le simulateur avec des paramètres différents.

L’illustration suivante est créée à l’aide de l’PRT direct uniquement (0 rebonds sans interréflexions).

![capture d’écran d’une illustration rendue à l’aide d’un PRT direct uniquement](images/prt-nointerreflections.png)

L’illustration suivante est créée à l’aide de PRT avec des interreflets (2 rebonds avec des interreflets).

![capture d’écran d’une illustration rendue à l’aide de PRT avec interreflets](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT avec diffusion sous-surface

La diffusion sous-surface est une technique qui modélise la façon dont la lumière passe par certains matériaux. En guise d’exemple, appuyez sur un appareil Torch allumé sur la paume de votre main. La lumière de la torche passe à la main, rebondne (en changeant la couleur du processus) et quitte l’autre côté de votre main. Cela peut également être modélisé avec des modifications simples dans le simulateur et aucune modification du Runtime.

L’illustration suivante montre PRT avec la diffusion sous-surface.

![capture d’écran d’une illustration rendue à l’aide de PRT avec diffusion sous-surface](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Fonctionnement de PRT

Les termes suivants sont utiles pour comprendre le fonctionnement de PRT, comme illustré dans le diagramme suivant.

Luminance source : le luminance source représente l’environnement d’éclairage dans son ensemble. Dans PRT, un environnement arbitraire est approximatif à l’aide de la base d’harmonique sphérique : cet éclairage est supposé être distant par rapport à l’objet (la même hypothèse que celle qui est faite avec les mappages d’environnement).

Quitter luminance : Exit luminance est la lumière qui quitte un point sur la surface de toute source possible (réfléchi luminance, diffusion subsurface, émission).

Transférer les vecteurs : les vecteurs de transfert mappent les luminance sources dans les luminance de sortie et sont précalculés hors connexion à l’aide d’une simulation de transport léger complexe.

![Diagramme illustrant le fonctionnement de PRT](images/prt-lightingpicture.png)

PRT détermine le processus de rendu en deux étapes, comme indiqué dans le diagramme suivant :

1.  Une simulation de transport de lumière coûteuse Précalcule le coefficient de transfert qui peut être utilisé au moment de l’exécution.
2.  Une phase d’exécution relativement légère est tout d’abord proche de l’environnement d’éclairage à l’aide de la base d’harmonique sphérique, puis utilise ces coefficients d’éclairage et les coefficients de transfert précalculés (de l’étape 1) avec un nuanceur simple, ce qui entraîne la sortie de luminance (la lumière quittant l’objet).

![diagramme du workflow de données PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Utilisation de l’API PRT

1.  Calculez les vecteurs de transfert avec l’une des valeurs de calcul... méthodes de [**ID3DXPRTEngine**](id3dxprtengine.md).

    Le traitement direct de ces vecteurs de transfert requiert une quantité significative de calcul de mémoire et de nuanceur. La compression réduit considérablement la quantité de mémoire et le calcul de nuanceur requis.

    Les valeurs d’éclairage finales sont calculées dans un nuanceur de sommets qui implémente l’équation de rendu compressé suivante.

    ![équation du rendu PRT](images/prt-shaderequation.png)

    Où :

    

    | Paramètre      | Description                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | PR             | Un seul canal de sortie luminance au sommet p et est évalué à chaque vertex de la maille.                     |
    | MK             | Moyenne du cluster k. Il s’agit d’un vecteur de coefficient de commande ².                                               |
    | k              | ID de cluster pour le vertex p.                                                                                    |
    | L<sup>'</sup>  | Approximation de la source luminance dans les fonctions de base SH. Il s’agit d’un vecteur de coefficient de commande ². |
    | j              | Entier qui additionne le nombre de vecteurs PCA.                                                            |
    | w<sub>PJ</sub> | Poids de JTH PCA pour le point p. Il s’agit d’un coefficient unique.                                                   |
    | B<sub>kJ</sub> | Le vecteur de base JTH PCA pour le cluster k. Il s’agit d’un vecteur de coefficient de commande ².                               |

    

     

    L’extraction... les méthodes de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) permettent d’accéder aux données compressées à partir de la simulation.

2.  Calculez la source luminance.

    Il existe plusieurs fonctions d’assistance dans l’API pour gérer un large éventail de scénarios d’éclairage courants.

    

    | Fonction                                                         | Objectif                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Arrondit une lumière directionnelle conventionnelle.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Approximation des sources de lumière sphérique locales. (Notez que PRT fonctionne uniquement avec les environnements d’éclairage à distance.) |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Se rapproche d’une source de lumière de zone éloignée. Un exemple est le soleil (très petit angle de cône).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Évalue une lumière qui est une interpolation linéaire entre deux couleurs (une sur chaque pôle d’une sphère).         |

    

     

3.  Calculez le luminance de sortie.

    L’équation 1 doit maintenant être évaluée à chaque point à l’aide d’un nuanceur de sommets ou de pixels. Avant de pouvoir évaluer le nuanceur, les constantes doivent être précalculées et chargées dans la table constante (pour plus d’informations, consultez l' [exemple de démonstration PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) ). Le nuanceur lui-même est une implémentation simple de cette équation.

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a>Références

Pour plus d’informations sur les harmoniques PRT et sphériques, consultez les documents suivants :


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> <dt>

[Équations PRT (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Représentation de PRT avec des textures (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Fonctions mathématiques](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



