---
title: Écriture de nuanceurs HLSL dans Direct3D 9
description: Écriture de nuanceurs HLSL dans Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031628"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Écriture de nuanceurs HLSL dans Direct3D 9

-   [Concepts de base des nuanceurs vertex](#vertex-shader-basics)
-   [Notions de base des nuanceurs de pixels](#pixel-shader-basics)
    -   [État de la texture et des États de l’échantillonneur](#texture-stage-and-sampler-states)
    -   [Entrées de nuanceur de pixels](#pixel-shader-inputs)
    -   [Sorties de nuanceur de pixels](#pixel-shader-outputs)
-   [Entrées de nuanceur et variables de nuanceur](#shader-inputs-and-shader-variables)
    -   [Déclaration de variables de nuanceur](#declaring-shader-variables)
    -   [Entrées uniformes de nuanceur](#uniform-shader-inputs)
    -   [Variation des entrées et de la sémantique des nuanceurs](#varying-shader-inputs-and-semantics)
    -   [Échantillonneurs et objets texture](#samplers-and-texture-objects)
-   [Écriture de fonctions](#writing-functions)
-   [Contrôle de Flow](#flow-control)
-   [Rubriques connexes](#related-topics)

## <a name="vertex-shader-basics"></a>Notions de base Vertex-Shader

En cas de fonctionnement, un nuanceur de sommet programmable remplace le traitement de vertex effectué par le pipeline de graphiques Microsoft Direct3D. Lors de l’utilisation d’un nuanceur de sommets, les informations d’État relatives aux opérations de transformation et d’éclairage sont ignorées par le pipeline de fonction fixe. Lorsque le nuanceur de sommets est désactivé et que le traitement de fonction fixe est retourné, tous les paramètres d’État actuels s’appliquent.

Le pavage des primitives d’ordre élevé doit être effectué avant l’exécution du nuanceur de sommets. Les implémentations qui effectuent un pavage de surface après le traitement du nuanceur doivent le faire d’une façon qui n’est pas apparente à l’application et au code du nuanceur.

Au minimum, un nuanceur de sommets doit sortir la position du vertex dans un espace de clip homogène. Le nuanceur de sommets peut éventuellement produire des coordonnées de texture, une couleur de vertex, un éclairage de vertex, des facteurs de brouillard, etc.

## <a name="pixel-shader-basics"></a>Notions de base Pixel-Shader

Le traitement des pixels est effectué par les nuanceurs de pixels sur des pixels individuels. Les nuanceurs de pixels fonctionnent de concert avec les nuanceurs de vertex. la sortie d’un nuanceur de sommets fournit les entrées d’un nuanceur de pixels. D’autres opérations de pixel (fusion de brouillard, opérations de stencil et fusion de cibles de rendu) se produisent après l’exécution du nuanceur.

### <a name="texture-stage-and-sampler-states"></a>État de la texture et des États de l’échantillonneur

Un nuanceur de pixels remplace complètement la fonctionnalité de fusion de pixels spécifiée par le mélangeur à plusieurs textures, y compris les opérations précédemment définies par les États de l’étape de texture. Les opérations de filtrage et d’échantillonnage de texture qui étaient contrôlées par les États de l’étape de texture standard pour la minimisation, le grossissement, le filtrage MIP et les modes d’adressage de renvoi à la ligne peuvent être initialisées dans les nuanceurs. L’application est libre de modifier ces États sans nécessiter la régénération du nuanceur actuellement lié. La définition de l’État peut être simplifiée si vos nuanceurs sont conçus dans un même but.

### <a name="pixel-shader-inputs"></a>Entrées de nuanceur de pixels

Pour les versions de nuanceur de pixels PS \_ 1 \_ 1-PS \_ 2 \_ 0, les couleurs diffuses et spéculaires sont saturées (bloquées) dans la plage de 0 à 1 avant d’être utilisées par le nuanceur.

Les valeurs de couleur entrées dans le nuanceur de pixels sont supposées être correctes, mais cela n’est pas garanti (pour tout le matériel). Les couleurs échantillonnées à partir des coordonnées de texture sont répétées de manière correcte et sont ancrées à la plage de 0 à 1 pendant l’itération.

### <a name="pixel-shader-outputs"></a>Sorties de nuanceur de pixels

Pour les versions de nuanceur de pixels PS \_ 1 \_ 1-PS \_ 1 \_ 4, le résultat émis par le nuanceur de pixels est le contenu de Register R0. Quel que soit l’moment où le nuanceur termine le traitement, il est envoyé à l’étape de brouillard et au mélangeur de cible de rendu.

Pour les versions de nuanceur de pixels PS \_ 2 \_ 0 et ultérieures, la couleur de sortie est émise à partir de OC0-oC4.

## <a name="shader-inputs-and-shader-variables"></a>Entrées de nuanceur et variables de nuanceur

-   [Déclaration de variables de nuanceur](#declaring-shader-variables)
-   [Entrées uniformes de nuanceur](#uniform-shader-inputs)
-   [Variation des entrées et de la sémantique des nuanceurs](#varying-shader-inputs-and-semantics)
-   [Échantillonneurs et objets texture](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Déclaration de variables de nuanceur

La déclaration de variable la plus simple comprend un type et un nom de variable, par exemple cette déclaration à virgule flottante :


```
float fVar;
```



Vous pouvez initialiser une variable dans la même instruction.


```
float fVar = 3.1f;
```



Un tableau de variables peut être déclaré,


```
int iVar[3];
```



ou déclarés et initialisés dans la même instruction.


```
int iVar[3] = {1,2,3};
```



Voici quelques déclarations qui illustrent la plupart des caractéristiques des variables HLSL (High-Level Shader Language) :


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Les déclarations de données peuvent utiliser n’importe quel type valide, y compris :

-   [Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Type de vecteur (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Type de matrice (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Type de nuanceur (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Type d’échantillonneur (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Type défini par l’utilisateur (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Un nuanceur peut avoir des variables, des arguments et des fonctions de niveau supérieur.


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



Les variables de niveau supérieur sont déclarées en dehors de toutes les fonctions. Les arguments de niveau supérieur sont des paramètres d’une fonction de niveau supérieur. Une fonction de niveau supérieur est toute fonction appelée par l’application (par opposition à une fonction qui est appelée par une autre fonction).

### <a name="uniform-shader-inputs"></a>Entrées uniformes de nuanceur

Les nuanceurs vertex et de pixels acceptent deux types de données d’entrée : variable et uniforme. L’entrée variable correspond aux données qui sont propres à chaque exécution du nuanceur. Pour un nuanceur de sommets, les données variables (par exemple, position, normal, etc.) proviennent des flux de vertex. Les données uniformes (par exemple, les couleurs matérielles, les transformations universelles, etc.) sont constantes pour les exécutions multiples d’un nuanceur. Pour ceux qui sont familiarisés avec les modèles de nuanceur d’assembly, les données uniformes sont spécifiées par des registres constants et des données variables par les registres v et t.

Les données uniformes peuvent être spécifiées par deux méthodes. La méthode la plus courante consiste à déclarer des variables globales et à les utiliser dans un nuanceur. Toute utilisation de variables globales dans un nuanceur entraîne l’ajout de cette variable à la liste des variables uniformes requises par ce nuanceur. La deuxième méthode consiste à marquer un paramètre d’entrée de la fonction de nuanceur de niveau supérieur comme uniforme. Ce marquage spécifie que la variable donnée doit être ajoutée à la liste des variables uniformes.

Les variables uniformes utilisées par un nuanceur sont communiquées à l’application via la table constante. La table de constantes est le nom de la table de symboles qui définit la façon dont les variables uniformes utilisées par un nuanceur s’intègrent aux registres de constantes. Les paramètres de fonction uniforme apparaissent dans le tableau constant précédé d’un signe dollar ($), contrairement aux variables globales. Le signe dollar est nécessaire pour éviter les conflits de noms entre les entrées uniformes locales et les variables globales du même nom.

La table constante contient les emplacements de Registre constants de toutes les variables uniformes utilisées par le nuanceur. Le tableau comprend également les informations de type et la valeur par défaut, si elles sont spécifiées.

### <a name="varying-shader-inputs-and-semantics"></a>Variation des entrées et de la sémantique des nuanceurs

La variation des paramètres d’entrée (d’une fonction de nuanceur de niveau supérieur) doit être marquée avec un mot clé sémantique ou uniforme, indiquant que la valeur est constante pour l’exécution du nuanceur. Si une entrée de nuanceur de niveau supérieur n’est pas marquée avec un mot clé sémantique ou uniforme, le nuanceur ne pourra pas être compilé.

La sémantique d’entrée est un nom utilisé pour lier l’entrée donnée à une sortie de la partie précédente du pipeline Graphics. Par exemple, le POSITION0 sémantique d’entrée est utilisé par les nuanceurs de vertex pour spécifier l’emplacement auquel les données de position de la mémoire tampon de vertex doivent être liées.

Les nuanceurs de pixels et vertex ont des jeux de sémantiques d’entrée différents en raison des différentes parties du pipeline graphique qui alimentent chaque unité de nuanceur. La sémantique d’entrée du nuanceur de sommets décrit les informations par vertex (par exemple, position, normal, coordonnées de texture, couleur, tangente, binormal, etc.) à charger à partir d’une mémoire tampon de vertex dans un format qui peut être consommé par le nuanceur de sommets. La sémantique d’entrée est directement mappée à l’utilisation de la déclaration de vertex et à l’index d’utilisation.

La sémantique d’entrée du nuanceur de pixels décrit les informations fournies par pixel par l’unité de rastérisation. Les données sont générées par l’interpolation entre les sorties du nuanceur de sommets pour chaque vertex de la primitive actuelle. La sémantique d’entrée de nuanceur de pixels de base lie la couleur de sortie et les informations de coordonnées de texture aux paramètres d’entrée.

La sémantique d’entrée peut être assignée à l’entrée de nuanceur par deux méthodes :

-   Ajout d’un signe deux-points et du nom sémantique à la déclaration du paramètre.
-   Définition d’une structure d’entrée avec la sémantique d’entrée assignée à chaque membre de la structure.

Les nuanceurs vertex et de pixels fournissent des données de sortie à l’étape de canalisation Graphics suivante. La sémantique de sortie est utilisée pour spécifier la façon dont les données générées par le nuanceur doivent être liées aux entrées de l’étape suivante. Par exemple, la sémantique de sortie d’un nuanceur de sommets est utilisée pour lier les sorties des interpolateurs dans le rastériseur afin de générer les données d’entrée pour le nuanceur de pixels. Les sorties de nuanceur de pixels sont les valeurs fournies à l’unité de fusion alpha pour chacune des cibles de rendu ou la valeur de profondeur écrite dans le tampon de profondeur.

La sémantique de sortie du nuanceur de sommets est utilisée pour lier le nuanceur à la fois au nuanceur de pixels et à l’étape de rastérisation. Un nuanceur de sommets qui est consommé par le rastériseur et qui n’est pas exposé au nuanceur de pixels doit générer des données de position au minimum. Les nuanceurs de sommets qui génèrent des coordonnées de texture et des données de couleur fournissent ces données à un nuanceur de pixels une fois l’interpolation effectuée.

La sémantique de sortie du nuanceur de pixels lie les couleurs de sortie d’un nuanceur de pixels à la cible de rendu appropriée. La couleur de sortie du nuanceur de pixels est liée à l’étape de fusion alpha, qui détermine la façon dont les cibles de rendu de destination sont modifiées. La sortie de la profondeur du nuanceur de pixels peut être utilisée pour modifier les valeurs de profondeur de destination à l’emplacement de trame actuel. La sortie de profondeur et plusieurs cibles de rendu sont uniquement prises en charge avec certains modèles de nuanceur.

La syntaxe de la sémantique de sortie est identique à celle de la spécification de la sémantique d’entrée. La sémantique peut être spécifiée directement sur les paramètres déclarés en tant que paramètres « out » ou assignées pendant la définition d’une structure qui est retournée en tant que paramètre « out » ou valeur de retour d’une fonction.

La sémantique identifie l’origine des données. Les sémantiques sont des identificateurs facultatifs qui identifient les entrées et les sorties du nuanceur. Les sémantiques s’affichent dans l’un des trois emplacements suivants :

-   Après un membre de structure.
-   Après un argument dans la liste d’arguments d’entrée d’une fonction.
-   Après la liste d’arguments d’entrée de la fonction.

Cet exemple utilise une structure pour fournir une ou plusieurs entrées de nuanceur de vertex, et une autre structure pour fournir une ou plusieurs sorties de nuanceur de vertex. Chacun des membres de la structure utilise une sémantique.


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



La structure d’entrée identifie les données de la mémoire tampon de vertex qui fourniront les entrées de nuanceur. Ce nuanceur mappe les données à partir des éléments position, normal et blendweight de la mémoire tampon de vertex dans des registres de nuanceur vertex. Le type de données d’entrée ne doit pas nécessairement correspondre exactement au type de données de la déclaration de vertex. Si elle ne correspond pas exactement à, les données du vertex sont automatiquement converties dans le type de données du langage HLSL lorsqu’elles sont écrites dans les registres des nuanceurs. Par exemple, si les données normales ont été définies comme étant de type UINT par l’application, elles sont converties en float3 lors de la lecture par le nuanceur.

Si les données du flux de vertex contiennent moins de composants que le type de données de nuanceur correspondant, les composants manquants seront initialisés à 0 (à l’exception de w, qui est initialisé à 1).

La sémantique d’entrée est semblable aux valeurs de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

La structure de sortie identifie les paramètres de sortie du nuanceur de sommets de position et de couleur. Ces sorties seront utilisées par le pipeline pour la pixellisation des triangles (en traitement primitif). La sortie marquée comme données de position indique la position d’un vertex dans un espace homogène. Au minimum, un nuanceur de sommets doit générer des données de position. La position de l’espace de l’écran est calculée après la fin du nuanceur de sommets en divisant la coordonnée (x, y, z) par w. Dans l’espace d’écran,-1 et 1 sont les valeurs x et y minimales et maximales des limites de la fenêtre d’affichage, tandis que z est utilisé pour le test de la mémoire tampon z.

La sémantique de sortie est également similaire aux valeurs dans [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage). En général, une structure de sortie pour un nuanceur de sommets peut également être utilisée comme structure d’entrée pour un nuanceur de pixels, à condition que le nuanceur de pixels ne lise pas les variables marquées avec la position, la taille du point ou la sémantique du brouillard. Ces sémantiques sont associées à des valeurs scalaires par vertex qui ne sont pas utilisées par un nuanceur de pixels. Si ces valeurs sont nécessaires pour le nuanceur de pixels, elles peuvent être copiées dans une autre variable de sortie qui utilise une sémantique de nuanceur de pixels.

Les variables globales sont assignées automatiquement aux registres par le compilateur. Les variables globales sont également appelées paramètres uniformes, car le contenu de la variable est le même pour tous les pixels traités chaque fois que le nuanceur est appelé. Les registres sont contenus dans la table constante, qui peut être lue à l’aide de l’interface [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .

La sémantique d’entrée pour les nuanceurs de pixels mappe les valeurs dans des registres matériels spécifiques pour le transport entre les nuanceurs de vertex et les nuanceurs de pixels. Chaque type de registre a des propriétés spécifiques. Étant donné qu’il n’existe actuellement que deux sémantiques pour les coordonnées de couleur et de texture, il est courant que la plupart des données soient marquées comme une coordonnée de texture même si ce n’est pas le cas.

Notez que la structure de sortie du nuanceur de sommets utilisait une entrée avec des données de position, ce qui n’est pas utilisé par le nuanceur de pixels. Le langage HLSL autorise des données de sortie valides d’un nuanceur de sommets qui ne sont pas des données d’entrée valides pour un nuanceur de pixels, à condition qu’il ne soit pas référencé dans le nuanceur de pixels.

Les arguments d’entrée peuvent également être des tableaux. La sémantique est automatiquement incrémentée par le compilateur pour chaque élément du tableau. Par exemple, considérez la déclaration explicite suivante :


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



La déclaration explicite fournie ci-dessus équivaut à la déclaration suivante dont la sémantique est automatiquement incrémentée par le compilateur :


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Tout comme la sémantique d’entrée, la sémantique de sortie identifie l’utilisation des données pour les données de sortie du nuanceur de pixels. De nombreux nuanceurs de pixels écrivent dans une seule couleur de sortie. Les nuanceurs de pixels peuvent également écrire une valeur de profondeur dans une ou plusieurs cibles de rendu multiples en même temps (jusqu’à quatre). Comme les nuanceurs vertex, les nuanceurs de pixels utilisent une structure pour retourner plusieurs sorties. Ce nuanceur écrit 0 dans les composants de couleur, ainsi que sur le composant profondeur.


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



Les couleurs de sortie du nuanceur de pixels doivent être de type float4. Lors de l’écriture de plusieurs couleurs, toutes les couleurs de sortie doivent être utilisées de manière contiguë. En d’autres termes, [COLOR1](dx-graphics-hlsl-semantics.md) ne peut pas être output, sauf si [COLOR0](dx-graphics-hlsl-semantics.md) a déjà été écrit. La sortie de la profondeur du nuanceur de pixels doit être de type float1.

### <a name="samplers-and-texture-objects"></a>Échantillonneurs et objets texture

Un échantillonneur contient l’état de l’échantillonneur. L’état de l’échantillonneur spécifie la texture à échantillonner et contrôle le filtrage effectué pendant l’échantillonnage. Trois éléments sont nécessaires pour échantillonner une texture :

-   Une texture
-   Un échantillonneur (avec l’état de l’échantillonneur)
-   Une instruction d’échantillonnage

Les échantillonneurs peuvent être initialisés avec les textures et l’état de l’échantillonneur comme indiqué ici :


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Voici un exemple de code pour échantillonner une texture 2D :


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



La texture est déclarée avec une variable de texture tex0.

Dans cet exemple, une variable d’échantillonnage nommée s \_ 2D est déclarée. L’échantillonneur contient l’état de l’échantillonneur à l’intérieur des accolades. Cela inclut la texture qui sera échantillonnée et, éventuellement, l’état du filtre (autrement dit, les modes de renvoi à la ligne, les modes de filtre, etc.). Si l’état de l’échantillonneur est omis, un état d’échantillonneur par défaut est appliqué en spécifiant le filtrage linéaire et un mode habillage pour les coordonnées de la texture. La fonction d’échantillonneur prend une coordonnée de texture à virgule flottante à deux composants et retourne une couleur à deux composants. Il est représenté par le type de retour float2 et représente les données dans les composants rouge et vert.

Quatre types d’échantillonneurs sont définis (consultez [Mots clés](dx-graphics-hlsl-appendix.md)) et les recherches de texture sont effectuées par les fonctions intrinsèques : [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md). Voici un exemple d’échantillonnage 3D :


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Cette déclaration d’échantillonneur utilise l’état d’échantillonnage par défaut pour les paramètres de filtre et le mode d’adresse.

Voici l’exemple d’échantillonnage de cube correspondant :


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Enfin, voici l’exemple d’échantillonnage 1D :


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Étant donné que le runtime ne prend pas en charge les textures 1D, le compilateur utilise une texture 2D avec la connaissance que la coordonnée y n’est pas importante. Étant donné que [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) est implémenté en tant que recherche de texture 2D, le compilateur est libre de choisir le composant y de manière efficace. Dans certains scénarios rares, le compilateur ne peut pas choisir un composant y efficace. dans ce cas, il émet un avertissement.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Cet exemple particulier est inefficace, car le compilateur doit déplacer la coordonnée d’entrée dans un autre registre (car une recherche 1D est implémentée en tant que recherche 2D et la coordonnée de texture est déclarée en tant que float1). Si le code est réécrit à l’aide d’une entrée float2 au lieu d’un float1, le compilateur peut utiliser la coordonnée de texture d’entrée, car il sait que y est initialisé à un.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Toutes les recherches de texture peuvent être ajoutées avec « Bias » ou « proj » (autrement dit, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)). Avec le suffixe « proj », la coordonnée de texture est divisée par le composant w. Avec « Bias », le niveau MIP est décalé par le composant w. Ainsi, toutes les recherches de texture avec un suffixe prennent toujours une entrée float4. [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) et [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorent respectivement les composants YZ et z.

Les échantillonneurs peuvent également être utilisés dans un tableau, même si aucun back end ne prend actuellement en charge l’accès aux tableaux dynamiques des échantillonneurs. Par conséquent, les éléments suivants sont valides, car ils peuvent être résolus au moment de la compilation :


```
tex2D(s[0],tex)
```



Toutefois, cet exemple n’est pas valide.


```
tex2D(s[a],tex)
```



L’accès dynamique des échantillonneurs est principalement utile pour écrire des programmes avec des boucles littérales. Le code suivant illustre l’accès au tableau d’échantillonneurs :


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> L’utilisation du runtime de débogage Microsoft Direct3D peut vous aider à intercepter les incompatibilités entre le nombre de composants dans une texture et un échantillonneur.

 

## <a name="writing-functions"></a>Écriture de fonctions

Les fonctions fractionnent les tâches de grande taille en plus petites. Les petites tâches sont plus faciles à déboguer et peuvent être réutilisées, une fois qu’elles sont éprouvées. Les fonctions peuvent être utilisées pour masquer les détails d’autres fonctions, ce qui rend un programme composé de fonctions plus facile à suivre.

Les fonctions HLSL sont similaires aux fonctions C de plusieurs façons : elles contiennent toutes les deux une définition et un corps de fonction, et elles déclarent toutes deux des types de retour et des listes d’arguments. À l’instar des fonctions C, la validation HLSL effectue une vérification de type sur les arguments, les types d’arguments et la valeur de retour pendant la compilation du nuanceur.

Contrairement aux fonctions C, les fonctions de point d’entrée HLSL utilisent la sémantique pour lier les arguments de fonction aux entrées et sorties du nuanceur (fonctions HLSL appelées « ignorer la sémantique en interne »). Cela facilite la liaison des données de mémoire tampon à un nuanceur et la liaison des sorties de nuanceur aux entrées de nuanceur.

Une fonction contient une déclaration et un corps, et la déclaration doit précéder le corps.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



La déclaration de fonction inclut tout ce qui se trouve devant les accolades :


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Une déclaration de fonction contient les éléments suivants :

-   Type de retour
-   Nom de fonction
-   Liste d’arguments (facultatif)
-   Une sémantique de sortie (facultatif)
-   Une annotation (facultatif)

Le type de retour peut être l’un des types de données de base HLSL tels qu’un float4 :


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



Le type de retour peut être une structure qui a déjà été définie :


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Si la fonction ne retourne pas de valeur, void peut être utilisé comme type de retour.


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Le type de retour apparaît toujours en premier dans une déclaration de fonction.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Une liste d’arguments déclare les arguments d’entrée à une fonction. Il peut également déclarer des valeurs qui seront retournées. Certains arguments sont à la fois des arguments d’entrée et de sortie. Voici un exemple de nuanceur qui accepte quatre arguments d’entrée.


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



Cette fonction retourne une couleur finale, qui est un mélange d’un échantillon de texture et de la couleur claire. La fonction accepte quatre entrées. Deux entrées ont une sémantique : LightDir a la sémantique [TEXCOORD1](dx-graphics-hlsl-semantics.md) , et texcrd a la sémantique [TEXCOORD0](dx-graphics-hlsl-semantics.md) . La sémantique signifie que les données de ces variables proviennent de la mémoire tampon de vertex. Même si la variable LightDir a une sémantique [TEXCOORD1](dx-graphics-hlsl-semantics.md) , le paramètre n’est probablement pas une coordonnée de texture. Le type sémantique TEXCOORDn est souvent utilisé pour fournir une sémantique pour un type qui n’est pas prédéfini (il n’y a pas de sémantique d’entrée de nuanceur de sommets pour une direction claire).

Les deux autres entrées LightColor et SAMP sont étiquetées avec le mot clé [Uniform](dx-graphics-hlsl-appendix.md) . Il s’agit de constantes uniformes qui ne changent pas entre les appels de dessin. Les valeurs de ces paramètres proviennent de variables globales de nuanceur.

Les arguments peuvent être étiquetés comme entrées avec le mot clé in, et les arguments de sortie avec le mot clé out. Les arguments ne peuvent pas être passés par référence ; Toutefois, un argument peut être à la fois une entrée et une sortie s’il est déclaré avec le mot clé INOUT. Les arguments passés à une fonction qui sont marqués avec le mot clé INOUT sont considérés comme des copies de l’original jusqu’au retour de la fonction, et ils sont recopiés. Voici un exemple d’utilisation de INOUT :


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Cette fonction incrémente les valeurs dans A et B et les retourne.

Le corps de la fonction est tout le code après la déclaration de la fonction.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Le corps se compose d’instructions qui sont entourées d’accolades. Le corps de la fonction implémente toutes les fonctionnalités à l’aide de variables, de littéraux, d’expressions et d’instructions.

Le corps du nuanceur effectue deux opérations : il effectue une multiplication de matrice et retourne un résultat float4. La multiplication de matrice est effectuée à l’aide de la fonction [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , qui effectue une multiplication de matrice 4x4. **mul (DirectX HLSL)** est appelé fonction intrinsèque, car il est déjà intégré à la bibliothèque de fonctions HLSL. Les fonctions intrinsèques seront couvertes plus en détail dans la section suivante.

La matrice multiplie combine un POS d’entrée et un WorldViewProj de matrice composite. Le résultat est la position des données transformées en espace à l’écran. Il s’agit du traitement de nuanceur de vertex minimal que nous pouvons effectuer. Si nous utilisons le pipeline de fonction fixe à la place d’un nuanceur de sommets, les données de vertex peuvent être dessinées après cette transformation.

La dernière instruction dans un corps de fonction est une instruction return. Tout comme C, cette instruction retourne le contrôle de la fonction à l’instruction qui a appelé la fonction.

Les types de retour de fonction peuvent être l’un des types de données simples définis en HLSL, notamment bool, int Half, float et double. Les types de retour peuvent être l’un des types de données complexes tels que les vecteurs et les matrices. Les types HLSL qui font référence aux objets ne peuvent pas être utilisés en tant que types de retour. Cela comprend PixelShader, VertexShader, texture et échantillonneur.

Voici un exemple de fonction qui utilise une structure pour un type de retour.


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



Le type de retour float4 a été remplacé par la structure et la \_ sortie, qui contient maintenant un seul membre float4.

Une instruction return signale la fin d’une fonction. Il s’agit de l’instruction return la plus simple. Elle retourne le contrôle de la fonction au programme appelant. Elle ne retourne aucune valeur.


```
void main()
{
    return ;
}
```



Une instruction return peut retourner une ou plusieurs valeurs. Cet exemple retourne une valeur littérale :


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



L’exemple suivant renvoie le résultat scalaire d’une expression :


```
return  light.enabled = true ;
```



Cet exemple retourne un float4 construit à partir d’une variable locale et d’un littéral :


```
return  float4(color.rgb, 1) ;
```



Cet exemple retourne un float4 qui est construit à partir du résultat retourné par une fonction intrinsèque, et quelques valeurs littérales :


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Cet exemple retourne une structure qui contient un ou plusieurs membres :


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>Contrôle de flux

Le matériel de nuanceur de vertex et de pixels actuel est conçu pour exécuter un nuanceur ligne par ligne, en exécutant chaque instruction une seule fois. Le langage HLSL prend en charge le contrôle de Flow, qui comprend la création de branches statiques, les instructions prédicats, le bouclage statique, la création de branche dynamique et le bouclage dynamique.

Auparavant, l’utilisation d’une instruction if entraînait le code du nuanceur de langage assembleur qui implémente à la fois le côté « si » et le côté « autre » du flot de code. Voici un exemple du code HLSL qui a été compilé pour vs \_ 1 \_ 1 :


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



Et voici le code assembleur obtenu :


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Certains matériels autorisent la boucle statique ou dynamique, mais la plupart nécessitent une exécution linéaire. Sur les modèles qui ne prennent pas en charge la boucle, toutes les boucles doivent être déroulées. C’est le cas, par exemple, de l’exemple [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) qui utilise des boucles non restaurées même pour les \_ \_ nuanceurs PS 1 1.

HLSL prend désormais en charge chacun de ces types de contrôle de flow :

-   Branchement statique
-   instructions prédicats
-   bouclage statique
-   Branchement dynamique
-   bouclage dynamique

La branche statique permet de basculer ou de désactiver des blocs de code de nuanceur en fonction d’une constante de nuanceur booléenne. Il s’agit d’une méthode pratique pour activer ou désactiver les chemins de code en fonction du type d’objet actuellement restitué. Entre les appels de dessin, vous pouvez choisir les fonctionnalités que vous souhaitez prendre en charge avec le nuanceur actuel, puis définir les indicateurs booléens requis pour obtenir ce comportement. Toutes les instructions qui sont désactivées par une constante booléenne sont ignorées lors de l’exécution du nuanceur.

La prise en charge de la branche la plus familière est la branche dynamique. Avec la création de branche dynamique, la condition de comparaison réside dans une variable, ce qui signifie que la comparaison est effectuée pour chaque vertex ou chaque pixel au moment de l’exécution (par opposition à la comparaison qui se produit au moment de la compilation, ou entre deux appels de dessin). L’impact sur les performances est le coût de la branche plus le coût des instructions sur le côté de la branche. La branche dynamique est implémentée dans le nuanceur modèle 3 ou version ultérieure. L’optimisation des nuanceurs qui fonctionnent avec ces modèles est semblable à l’optimisation du code qui s’exécute sur un processeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 