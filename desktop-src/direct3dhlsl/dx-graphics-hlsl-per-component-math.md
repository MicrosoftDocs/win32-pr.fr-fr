---
title: Opérations mathématiques Per-Component
description: En HLSL, vous pouvez programmer des nuanceurs au niveau d’un algorithme.
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2021
ms.locfileid: "104982818"
---
# <a name="per-component-math-operations"></a>Opérations mathématiques Per-Component

En HLSL, vous pouvez programmer des nuanceurs au niveau d’un algorithme. Pour comprendre le langage, vous devrez savoir comment déclarer des variables et des fonctions, utiliser des fonctions intrinsèques, définir des types de données personnalisés et utiliser la sémantique pour connecter des arguments de nuanceur à d’autres nuanceurs et au pipeline.

Une fois que vous avez appris à créer des nuanceurs en HLSL, vous devez en savoir plus sur les appels d’API afin de pouvoir : compiler un nuanceur pour un matériel particulier, initialiser des constantes de nuanceur et initialiser un autre État de pipeline si nécessaire.

-   [Type de vecteur](#the-vector-type)
-   [Type de matrice](#the-matrix-type)
    -   [Classement de la matrice](#matrix-ordering)
-   [Exemples](#examples)
-   [Rubriques connexes](#related-topics)

## <a name="the-vector-type"></a>Type de vecteur

Un vecteur est une structure de données qui contient entre un et quatre composants.


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



L’entier qui suit immédiatement le type de données est le nombre de composants sur le vecteur.

Les initialiseurs peuvent également être inclus dans les déclarations.


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Le type Vector peut également être utilisé pour effectuer les mêmes déclarations :


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



Le type de vecteur utilise des crochets pointus pour spécifier le type et le nombre de composants.

Les vecteurs contiennent jusqu’à quatre composants, chacun d’entre eux étant accessible à l’aide de l’un des deux ensembles d’attribution de noms :

-   La position définie : x, y, z, w
-   Jeu de couleurs : r, g, b, a

Ces instructions retournent toutes deux la valeur dans le troisième composant.


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



Les ensembles de noms peuvent utiliser un ou plusieurs composants, mais ils ne peuvent pas être mélangés.


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



La spécification d’un ou plusieurs composants vectoriels lors de la lecture des composants s’appelle swizzling. Par exemple :


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



Le masquage contrôle le nombre de composants écrits.


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



Les assignations ne peuvent pas être écrites plusieurs fois dans le même composant. Le côté gauche de cette instruction n’est donc pas valide :


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



En outre, les espaces de noms de composants ne peuvent pas être mélangés. Il s’agit d’une écriture de composant non valide :


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



L’accès à un vecteur en tant que scalaire permet d’accéder au premier composant du vecteur. Les deux instructions suivantes sont équivalentes.


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>Type de matrice

Une matrice est une structure de données qui contient des lignes et des colonnes de données. Les données peuvent être de l’un des types de données scalaires, mais chaque élément d’une matrice est du même type de données. Le nombre de lignes et de colonnes est spécifié avec la chaîne ligne par colonne qui est ajoutée au type de données.


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



Le nombre maximal de lignes ou de colonnes est de 4 ; le nombre minimal est 1.

Une matrice peut être initialisée lorsqu’elle est déclarée :


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Ou le type de matrice peut être utilisé pour effectuer les mêmes déclarations :


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



Le type de matrice utilise les crochets angulaires pour spécifier le type, le nombre de lignes et le nombre de colonnes. Cet exemple crée une matrice à virgule flottante, avec deux lignes et deux colonnes. Tous les types de données scalaires peuvent être utilisés.

Cette déclaration définit une matrice de valeurs float (nombres à virgule flottante 32 bits) avec deux lignes et trois colonnes :


```
matrix <float, 2, 3> fFloatMatrix;
```



Une matrice contient des valeurs organisées en lignes et en colonnes, qui sont accessibles à l’aide de l’opérateur de structure « . » suivi de l’un des deux ensembles d’attribution de noms :

-   Position de la colonne de ligne de base zéro :
    -   \_M00, \_ M01, \_ M02, \_ M03
    -   \_M10, \_ M11, \_ M12, \_ M13
    -   \_M20, \_ M21, \_ M22, \_ M23
    -   \_M30, \_ M31, \_ M32, \_ M33
-   Position de colonne de ligne de base 1 :
    -   \_11, \_ 12, \_ 13, \_ 14
    -   \_21, \_ 22, \_ 23, \_ 24
    -   \_31, \_ 32, \_ 33, \_ 34
    -   \_41, \_ 42, \_ 43, \_ 44

Chaque ensemble d’attribution de noms commence par un trait de soulignement suivi du numéro de ligne et du numéro de colonne. La Convention de base zéro comprend également la lettre « m » avant le numéro de ligne et de colonne. Voici un exemple qui utilise les deux ensembles de noms pour accéder à une matrice :


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



Tout comme les vecteurs, les ensembles de noms peuvent utiliser un ou plusieurs composants de l’ensemble de noms.


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



Une matrice est également accessible à l’aide de la notation d’accès au tableau, qui est un jeu d’index de base zéro. Chaque index se trouve à l’intérieur de crochets. Une matrice 4x4 est accessible avec les index suivants :

-   \[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] \[ \] \[ \] \[ \] \[ , 0, 0 3\]
-   \[1 \] \[ 0,1 \] 1, 1 \[ \] \[ \] \[ \] \[ 2, 1 \] \[ \] \[ 3\]
-   \[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] \[ \] \[ \] \[ \] \[ , 2 2, 2 3\]
-   \[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ \] \[ \] \[ \] \[ 3 2,3\]

Voici un exemple d’accès à une matrice :


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



Notez que l’opérateur de structure « . » n’est pas utilisé pour accéder à un tableau. La notation d’accès au tableau ne peut pas utiliser swizzling pour lire plusieurs composants.


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



Toutefois, l’accès à un tableau peut lire un vecteur à plusieurs composants.


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



Comme avec les vecteurs, la lecture de plusieurs composants de matrice est appelée swizzling. Plusieurs composants peuvent être affectés, en supposant qu’un seul espace de noms est utilisé. Il s’agit de toutes les attributions valides :


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



Le masquage contrôle le nombre de composants écrits.


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



Les assignations ne peuvent pas être écrites plusieurs fois dans le même composant. Le côté gauche de cette instruction n’est donc pas valide :


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



En outre, les espaces de noms de composants ne peuvent pas être mélangés. Il s’agit d’une écriture de composant non valide :


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>Classement de la matrice

L’ordre de compression des matrices pour les paramètres uniformes est défini sur Column-major par défaut. Cela signifie que chaque colonne de la matrice est stockée dans un registre de constante unique. En revanche, une matrice de lignes principales compresse chaque ligne de la matrice dans un registre de constante unique. La compression de matrice peut être modifiée à l’aide de la directive de **\# \_ matrice pragmapack** , ou avec la **ligne \_ principale** ou le mot clé **\_ principal de colonne** .

Les données d’une matrice sont chargées dans des registres de constantes de nuanceur avant l’exécution d’un nuanceur. Il existe deux choix pour la façon dont les données de la matrice sont lues : dans l’ordre ligne-principal ou dans l’ordre des colonnes. Column-major signifie que chaque colonne de matrice est stockée dans un registre de constante unique et que l’ordre de ligne-colonne signifie que chaque ligne de la matrice est stockée dans un registre de constante unique. Il s’agit d’un point important à prendre en compte pour le nombre de registres constants utilisés pour une matrice.

Une matrice de lignes principales est présentée comme suit :



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 12  | 13  | 14  |
| 21  | 22  | 23  | 24  |
| 31  | 32  | 33  | 34  |
| 41  | 42  | 43  | 44  |



 

Une matrice de colonne principale est présentée comme suit :



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 21  | 31  | 41  |
| 12  | 22  | 32  | 42  |
| 13  | 23  | 33  | 43  |
| 14  | 24  | 34  | 44  |



 

Le classement des matrices de lignes et de colonnes principales détermine l’ordre dans lequel les composants de matrice sont lus à partir des entrées de nuanceur. Une fois les données écrites dans des registres constants, l’ordre de la matrice n’a aucun effet sur la façon dont les données sont utilisées ou accessibles à partir du code du nuanceur. En outre, les matrices déclarées dans un corps de nuanceur ne sont pas empaquetées dans des registres constants. Les commandes de compression de ligne-principale et de colonne-principal n’ont aucune incidence sur l’ordre de compression des constructeurs (qui suit toujours le classement de ligne par ligne).

L’ordre des données dans une matrice peut être déclaré au moment de la compilation ou le compilateur classe les données au moment de l’exécution pour l’utilisation la plus efficace.

## <a name="examples"></a>Exemples

Le langage HLSL utilise deux types spéciaux, un type de vecteur et un type de matrice pour faciliter la programmation de graphiques 2D et 3D. Chacun de ces types contient plus d’un composant ; un vecteur contient jusqu’à quatre composants et une matrice contient jusqu’à 16 composants. Lorsque des vecteurs et des matrices sont utilisés dans des équations HLSL standard, le calcul mathématique est conçu pour fonctionner par composant. Par exemple, HLSL implémente cette multiplication :


```
float4 v = a*b;
```



en tant que multiplication à quatre composants. Le résultat est quatre scalaires :


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



Il s’agit de quatre multiplicités où chaque résultat est stocké dans un composant séparé de v. C’est ce qu’on appelle une multiplication à quatre composants. Le langage HLSL utilise des mathématiques de composant qui rendent l’écriture des nuanceurs très efficace.

Cela est très différent d’une multiplication qui est généralement implémentée comme un produit scalaire qui génère une seule scalaire :


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



Une matrice utilise également des opérations par composant en HLSL :


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



Le résultat est une multiplication par composant des deux matrices (par opposition à une matrice de matrice 3x3 standard). Une multiplication par matrice de composant produit ce premier terme :


```
mat3.m00 = mat1.m00 * mat2._m00;
```



Cela est différent d’une multiplication de matrice 3x3 qui produit ce premier terme :


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



Les versions surchargées des fonctions intrinsèques de multiplication gèrent les cas où un opérande est un vecteur et l’autre opérande est une matrice. Par exemple : \* Vector Vector, vector \* Matrix, Matrix \* Vector et Matrix Matrix \* . Exemple :


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



produit le même résultat que :


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



Cet exemple convertit le vecteur POS en un vecteur de colonne à l’aide du cast (float1x4). La modification d’un vecteur par cast ou l’échange de l’ordre des arguments fournis à Multiply équivaut à transposer la matrice.

La conversion de cast automatique fait que les fonctions de multiplication et de point intrinsèques renvoient les mêmes résultats que ceux utilisés ici :


```
{
  float4 val;
  return mul(val,val);
}
```



Le résultat de la multiplication est un \* vecteur 1x4 4x1 = 1x1. Cela équivaut à un produit scalaire :


```
{
  float4 val;
  return dot(val,val);
}
```



qui retourne une valeur scalaire unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




