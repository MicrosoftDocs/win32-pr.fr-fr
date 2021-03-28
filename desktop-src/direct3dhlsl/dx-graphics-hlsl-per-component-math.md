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
# <a name="per-component-math-operations"></a><span data-ttu-id="8286e-103">Opérations mathématiques Per-Component</span><span class="sxs-lookup"><span data-stu-id="8286e-103">Per-Component Math Operations</span></span>

<span data-ttu-id="8286e-104">En HLSL, vous pouvez programmer des nuanceurs au niveau d’un algorithme.</span><span class="sxs-lookup"><span data-stu-id="8286e-104">With HLSL, you can program shaders at an algorithm level.</span></span> <span data-ttu-id="8286e-105">Pour comprendre le langage, vous devrez savoir comment déclarer des variables et des fonctions, utiliser des fonctions intrinsèques, définir des types de données personnalisés et utiliser la sémantique pour connecter des arguments de nuanceur à d’autres nuanceurs et au pipeline.</span><span class="sxs-lookup"><span data-stu-id="8286e-105">To understand the language, you will need to know how to declare variables and functions, use intrinsic functions, define custom data types and use semantics to connect shader arguments to other shaders and to the pipeline.</span></span>

<span data-ttu-id="8286e-106">Une fois que vous avez appris à créer des nuanceurs en HLSL, vous devez en savoir plus sur les appels d’API afin de pouvoir : compiler un nuanceur pour un matériel particulier, initialiser des constantes de nuanceur et initialiser un autre État de pipeline si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8286e-106">Once you learn how to author shaders in HLSL, you will need to learn about API calls so that you can: compile a shader for particular hardware, initialize shader constants, and initialize other pipeline state if necessary.</span></span>

-   [<span data-ttu-id="8286e-107">Type de vecteur</span><span class="sxs-lookup"><span data-stu-id="8286e-107">The Vector Type</span></span>](#the-vector-type)
-   [<span data-ttu-id="8286e-108">Type de matrice</span><span class="sxs-lookup"><span data-stu-id="8286e-108">The Matrix Type</span></span>](#the-matrix-type)
    -   [<span data-ttu-id="8286e-109">Classement de la matrice</span><span class="sxs-lookup"><span data-stu-id="8286e-109">Matrix Ordering</span></span>](#matrix-ordering)
-   [<span data-ttu-id="8286e-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="8286e-110">Examples</span></span>](#examples)
-   [<span data-ttu-id="8286e-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8286e-111">Related topics</span></span>](#related-topics)

## <a name="the-vector-type"></a><span data-ttu-id="8286e-112">Type de vecteur</span><span class="sxs-lookup"><span data-stu-id="8286e-112">The Vector Type</span></span>

<span data-ttu-id="8286e-113">Un vecteur est une structure de données qui contient entre un et quatre composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-113">A vector is a data structure that contains between one and four components.</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



<span data-ttu-id="8286e-114">L’entier qui suit immédiatement le type de données est le nombre de composants sur le vecteur.</span><span class="sxs-lookup"><span data-stu-id="8286e-114">The integer immediately following the data type is the number of components on the vector.</span></span>

<span data-ttu-id="8286e-115">Les initialiseurs peuvent également être inclus dans les déclarations.</span><span class="sxs-lookup"><span data-stu-id="8286e-115">Initializers can also be included in the declarations.</span></span>


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8286e-116">Le type Vector peut également être utilisé pour effectuer les mêmes déclarations :</span><span class="sxs-lookup"><span data-stu-id="8286e-116">Alternatively, the vector type can be used to make the same declarations:</span></span>


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



<span data-ttu-id="8286e-117">Le type de vecteur utilise des crochets pointus pour spécifier le type et le nombre de composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-117">The vector type uses angle brackets to specify the type and number of components.</span></span>

<span data-ttu-id="8286e-118">Les vecteurs contiennent jusqu’à quatre composants, chacun d’entre eux étant accessible à l’aide de l’un des deux ensembles d’attribution de noms :</span><span class="sxs-lookup"><span data-stu-id="8286e-118">Vectors contain up to four components, each of which can be accessed using one of two naming sets:</span></span>

-   <span data-ttu-id="8286e-119">La position définie : x, y, z, w</span><span class="sxs-lookup"><span data-stu-id="8286e-119">The position set: x,y,z,w</span></span>
-   <span data-ttu-id="8286e-120">Jeu de couleurs : r, g, b, a</span><span class="sxs-lookup"><span data-stu-id="8286e-120">The color set: r,g,b,a</span></span>

<span data-ttu-id="8286e-121">Ces instructions retournent toutes deux la valeur dans le troisième composant.</span><span class="sxs-lookup"><span data-stu-id="8286e-121">These statements both return the value in the third component.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



<span data-ttu-id="8286e-122">Les ensembles de noms peuvent utiliser un ou plusieurs composants, mais ils ne peuvent pas être mélangés.</span><span class="sxs-lookup"><span data-stu-id="8286e-122">Naming sets can use one or more components, but they cannot be mixed.</span></span>


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



<span data-ttu-id="8286e-123">La spécification d’un ou plusieurs composants vectoriels lors de la lecture des composants s’appelle swizzling.</span><span class="sxs-lookup"><span data-stu-id="8286e-123">Specifying one or more vector components when reading components is called swizzling.</span></span> <span data-ttu-id="8286e-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8286e-124">For example:</span></span>


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



<span data-ttu-id="8286e-125">Le masquage contrôle le nombre de composants écrits.</span><span class="sxs-lookup"><span data-stu-id="8286e-125">Masking controls how many components are written.</span></span>


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



<span data-ttu-id="8286e-126">Les assignations ne peuvent pas être écrites plusieurs fois dans le même composant.</span><span class="sxs-lookup"><span data-stu-id="8286e-126">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8286e-127">Le côté gauche de cette instruction n’est donc pas valide :</span><span class="sxs-lookup"><span data-stu-id="8286e-127">So the left side of this statement is invalid:</span></span>


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



<span data-ttu-id="8286e-128">En outre, les espaces de noms de composants ne peuvent pas être mélangés.</span><span class="sxs-lookup"><span data-stu-id="8286e-128">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8286e-129">Il s’agit d’une écriture de composant non valide :</span><span class="sxs-lookup"><span data-stu-id="8286e-129">This is an invalid component write:</span></span>


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



<span data-ttu-id="8286e-130">L’accès à un vecteur en tant que scalaire permet d’accéder au premier composant du vecteur.</span><span class="sxs-lookup"><span data-stu-id="8286e-130">Accessing a vector as a scalar will access the first component of the vector.</span></span> <span data-ttu-id="8286e-131">Les deux instructions suivantes sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="8286e-131">The following two statements are equivalent.</span></span>


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a><span data-ttu-id="8286e-132">Type de matrice</span><span class="sxs-lookup"><span data-stu-id="8286e-132">The Matrix Type</span></span>

<span data-ttu-id="8286e-133">Une matrice est une structure de données qui contient des lignes et des colonnes de données.</span><span class="sxs-lookup"><span data-stu-id="8286e-133">A matrix is a data structure that contains rows and columns of data.</span></span> <span data-ttu-id="8286e-134">Les données peuvent être de l’un des types de données scalaires, mais chaque élément d’une matrice est du même type de données.</span><span class="sxs-lookup"><span data-stu-id="8286e-134">The data can be any of the scalar data types, however, every element of a matrix is the same data type.</span></span> <span data-ttu-id="8286e-135">Le nombre de lignes et de colonnes est spécifié avec la chaîne ligne par colonne qui est ajoutée au type de données.</span><span class="sxs-lookup"><span data-stu-id="8286e-135">The number of rows and columns is specified with the row-by-column string that is appended to the data type.</span></span>


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



<span data-ttu-id="8286e-136">Le nombre maximal de lignes ou de colonnes est de 4 ; le nombre minimal est 1.</span><span class="sxs-lookup"><span data-stu-id="8286e-136">The maximum number of rows or columns is 4; the minimum number is 1.</span></span>

<span data-ttu-id="8286e-137">Une matrice peut être initialisée lorsqu’elle est déclarée :</span><span class="sxs-lookup"><span data-stu-id="8286e-137">A matrix can be initialized when it is declared:</span></span>


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="8286e-138">Ou le type de matrice peut être utilisé pour effectuer les mêmes déclarations :</span><span class="sxs-lookup"><span data-stu-id="8286e-138">Or, the matrix type can be used to make the same declarations:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



<span data-ttu-id="8286e-139">Le type de matrice utilise les crochets angulaires pour spécifier le type, le nombre de lignes et le nombre de colonnes.</span><span class="sxs-lookup"><span data-stu-id="8286e-139">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="8286e-140">Cet exemple crée une matrice à virgule flottante, avec deux lignes et deux colonnes.</span><span class="sxs-lookup"><span data-stu-id="8286e-140">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="8286e-141">Tous les types de données scalaires peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="8286e-141">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="8286e-142">Cette déclaration définit une matrice de valeurs float (nombres à virgule flottante 32 bits) avec deux lignes et trois colonnes :</span><span class="sxs-lookup"><span data-stu-id="8286e-142">This declaration defines a matrix of float values (32-bit floating-point numbers) with two rows and three columns:</span></span>


```
matrix <float, 2, 3> fFloatMatrix;
```



<span data-ttu-id="8286e-143">Une matrice contient des valeurs organisées en lignes et en colonnes, qui sont accessibles à l’aide de l’opérateur de structure « . » suivi de l’un des deux ensembles d’attribution de noms :</span><span class="sxs-lookup"><span data-stu-id="8286e-143">A matrix contains values organized in rows and columns, which can be accessed using the structure operator "." followed by one of two naming sets:</span></span>

-   <span data-ttu-id="8286e-144">Position de la colonne de ligne de base zéro :</span><span class="sxs-lookup"><span data-stu-id="8286e-144">The zero-based row-column position:</span></span>
    -   <span data-ttu-id="8286e-145">\_M00, \_ M01, \_ M02, \_ M03</span><span class="sxs-lookup"><span data-stu-id="8286e-145">\_m00, \_m01, \_m02, \_m03</span></span>
    -   <span data-ttu-id="8286e-146">\_M10, \_ M11, \_ M12, \_ M13</span><span class="sxs-lookup"><span data-stu-id="8286e-146">\_m10, \_m11, \_m12, \_m13</span></span>
    -   <span data-ttu-id="8286e-147">\_M20, \_ M21, \_ M22, \_ M23</span><span class="sxs-lookup"><span data-stu-id="8286e-147">\_m20, \_m21, \_m22, \_m23</span></span>
    -   <span data-ttu-id="8286e-148">\_M30, \_ M31, \_ M32, \_ M33</span><span class="sxs-lookup"><span data-stu-id="8286e-148">\_m30, \_m31, \_m32, \_m33</span></span>
-   <span data-ttu-id="8286e-149">Position de colonne de ligne de base 1 :</span><span class="sxs-lookup"><span data-stu-id="8286e-149">The one-based row-column position:</span></span>
    -   <span data-ttu-id="8286e-150">\_11, \_ 12, \_ 13, \_ 14</span><span class="sxs-lookup"><span data-stu-id="8286e-150">\_11, \_12, \_13, \_14</span></span>
    -   <span data-ttu-id="8286e-151">\_21, \_ 22, \_ 23, \_ 24</span><span class="sxs-lookup"><span data-stu-id="8286e-151">\_21, \_22, \_23, \_24</span></span>
    -   <span data-ttu-id="8286e-152">\_31, \_ 32, \_ 33, \_ 34</span><span class="sxs-lookup"><span data-stu-id="8286e-152">\_31, \_32, \_33, \_34</span></span>
    -   <span data-ttu-id="8286e-153">\_41, \_ 42, \_ 43, \_ 44</span><span class="sxs-lookup"><span data-stu-id="8286e-153">\_41, \_42, \_43, \_44</span></span>

<span data-ttu-id="8286e-154">Chaque ensemble d’attribution de noms commence par un trait de soulignement suivi du numéro de ligne et du numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="8286e-154">Each naming set starts with an underscore followed by the row number and the column number.</span></span> <span data-ttu-id="8286e-155">La Convention de base zéro comprend également la lettre « m » avant le numéro de ligne et de colonne.</span><span class="sxs-lookup"><span data-stu-id="8286e-155">The zero-based convention also includes the letter "m" before the row and column number.</span></span> <span data-ttu-id="8286e-156">Voici un exemple qui utilise les deux ensembles de noms pour accéder à une matrice :</span><span class="sxs-lookup"><span data-stu-id="8286e-156">Here's an example that uses the two naming sets to access a matrix:</span></span>


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



<span data-ttu-id="8286e-157">Tout comme les vecteurs, les ensembles de noms peuvent utiliser un ou plusieurs composants de l’ensemble de noms.</span><span class="sxs-lookup"><span data-stu-id="8286e-157">Just like vectors, naming sets can use one or more components from either naming set.</span></span>


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



<span data-ttu-id="8286e-158">Une matrice est également accessible à l’aide de la notation d’accès au tableau, qui est un jeu d’index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="8286e-158">A matrix can also be accessed using array access notation, which is a zero-based set of indices.</span></span> <span data-ttu-id="8286e-159">Chaque index se trouve à l’intérieur de crochets.</span><span class="sxs-lookup"><span data-stu-id="8286e-159">Each index is inside of square brackets.</span></span> <span data-ttu-id="8286e-160">Une matrice 4x4 est accessible avec les index suivants :</span><span class="sxs-lookup"><span data-stu-id="8286e-160">A 4x4 matrix is accessed with the following indices:</span></span>

-   <span data-ttu-id="8286e-161">\[0 \] \[ 0 \] , \[ 0 \] \[ 1 \] \[ \] \[ \] \[ \] \[ , 0, 0 3\]</span><span class="sxs-lookup"><span data-stu-id="8286e-161">\[0\]\[0\], \[0\]\[1\], \[0\]\[2\], \[0\]\[3\]</span></span>
-   <span data-ttu-id="8286e-162">\[1 \] \[ 0,1 \] 1, 1 \[ \] \[ \] \[ \] \[ 2, 1 \] \[ \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="8286e-162">\[1\]\[0\], \[1\]\[1\], \[1\]\[2\], \[1\]\[3\]</span></span>
-   <span data-ttu-id="8286e-163">\[2 \] \[ 0 \] , \[ 2 \] \[ 1 \] \[ \] \[ \] \[ \] \[ , 2 2, 2 3\]</span><span class="sxs-lookup"><span data-stu-id="8286e-163">\[2\]\[0\], \[2\]\[1\], \[2\]\[2\], \[2\]\[3\]</span></span>
-   <span data-ttu-id="8286e-164">\[3 \] \[ 0 \] , \[ 3 \] \[ 1 \] , \[ \] \[ \] \[ \] \[ 3 2,3\]</span><span class="sxs-lookup"><span data-stu-id="8286e-164">\[3\]\[0\], \[3\]\[1\], \[3\]\[2\], \[3\]\[3\]</span></span>

<span data-ttu-id="8286e-165">Voici un exemple d’accès à une matrice :</span><span class="sxs-lookup"><span data-stu-id="8286e-165">Here is an example of accessing a matrix:</span></span>


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



<span data-ttu-id="8286e-166">Notez que l’opérateur de structure « . » n’est pas utilisé pour accéder à un tableau.</span><span class="sxs-lookup"><span data-stu-id="8286e-166">Notice that the structure operator "." is not used to access an array.</span></span> <span data-ttu-id="8286e-167">La notation d’accès au tableau ne peut pas utiliser swizzling pour lire plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-167">Array access notation cannot use swizzling to read more than one component.</span></span>


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



<span data-ttu-id="8286e-168">Toutefois, l’accès à un tableau peut lire un vecteur à plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-168">However, array accessing can read a multi-component vector.</span></span>


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



<span data-ttu-id="8286e-169">Comme avec les vecteurs, la lecture de plusieurs composants de matrice est appelée swizzling.</span><span class="sxs-lookup"><span data-stu-id="8286e-169">As with vectors, reading more than one matrix component is called swizzling.</span></span> <span data-ttu-id="8286e-170">Plusieurs composants peuvent être affectés, en supposant qu’un seul espace de noms est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8286e-170">More than one component can be assigned, assuming only one name space is used.</span></span> <span data-ttu-id="8286e-171">Il s’agit de toutes les attributions valides :</span><span class="sxs-lookup"><span data-stu-id="8286e-171">These are all valid assignments:</span></span>


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



<span data-ttu-id="8286e-172">Le masquage contrôle le nombre de composants écrits.</span><span class="sxs-lookup"><span data-stu-id="8286e-172">Masking controls how many components are written.</span></span>


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8286e-173">Les assignations ne peuvent pas être écrites plusieurs fois dans le même composant.</span><span class="sxs-lookup"><span data-stu-id="8286e-173">Assignments cannot be written to the same component more than once.</span></span> <span data-ttu-id="8286e-174">Le côté gauche de cette instruction n’est donc pas valide :</span><span class="sxs-lookup"><span data-stu-id="8286e-174">So the left side of this statement is invalid:</span></span>


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



<span data-ttu-id="8286e-175">En outre, les espaces de noms de composants ne peuvent pas être mélangés.</span><span class="sxs-lookup"><span data-stu-id="8286e-175">Also, the component name spaces cannot be mixed.</span></span> <span data-ttu-id="8286e-176">Il s’agit d’une écriture de composant non valide :</span><span class="sxs-lookup"><span data-stu-id="8286e-176">This is an invalid component write:</span></span>


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a><span data-ttu-id="8286e-177">Classement de la matrice</span><span class="sxs-lookup"><span data-stu-id="8286e-177">Matrix Ordering</span></span>

<span data-ttu-id="8286e-178">L’ordre de compression des matrices pour les paramètres uniformes est défini sur Column-major par défaut.</span><span class="sxs-lookup"><span data-stu-id="8286e-178">Matrix packing order for uniform parameters is set to column-major by default.</span></span> <span data-ttu-id="8286e-179">Cela signifie que chaque colonne de la matrice est stockée dans un registre de constante unique.</span><span class="sxs-lookup"><span data-stu-id="8286e-179">This means each column of the matrix is stored in a single constant register.</span></span> <span data-ttu-id="8286e-180">En revanche, une matrice de lignes principales compresse chaque ligne de la matrice dans un registre de constante unique.</span><span class="sxs-lookup"><span data-stu-id="8286e-180">On the other hand, a row-major matrix packs each row of the matrix in a single constant register.</span></span> <span data-ttu-id="8286e-181">La compression de matrice peut être modifiée à l’aide de la directive de **\# \_ matrice pragmapack** , ou avec la **ligne \_ principale** ou le mot clé **\_ principal de colonne** .</span><span class="sxs-lookup"><span data-stu-id="8286e-181">Matrix packing can be changed with the **\#pragmapack\_matrix** directive, or with the **row\_major** or the **column\_major** keyword.</span></span>

<span data-ttu-id="8286e-182">Les données d’une matrice sont chargées dans des registres de constantes de nuanceur avant l’exécution d’un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8286e-182">The data in a matrix is loaded into shader constant registers before a shader runs.</span></span> <span data-ttu-id="8286e-183">Il existe deux choix pour la façon dont les données de la matrice sont lues : dans l’ordre ligne-principal ou dans l’ordre des colonnes.</span><span class="sxs-lookup"><span data-stu-id="8286e-183">There are two choices for how the matrix data is read: in row-major order or in column-major order.</span></span> <span data-ttu-id="8286e-184">Column-major signifie que chaque colonne de matrice est stockée dans un registre de constante unique et que l’ordre de ligne-colonne signifie que chaque ligne de la matrice est stockée dans un registre de constante unique.</span><span class="sxs-lookup"><span data-stu-id="8286e-184">Column-major order means that each matrix column will be stored in a single constant register, and row-major order means that each row of the matrix will be stored in a single constant register.</span></span> <span data-ttu-id="8286e-185">Il s’agit d’un point important à prendre en compte pour le nombre de registres constants utilisés pour une matrice.</span><span class="sxs-lookup"><span data-stu-id="8286e-185">This is an important consideration for how many constant registers are used for a matrix.</span></span>

<span data-ttu-id="8286e-186">Une matrice de lignes principales est présentée comme suit :</span><span class="sxs-lookup"><span data-stu-id="8286e-186">A row-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="8286e-187">11</span><span class="sxs-lookup"><span data-stu-id="8286e-187">11</span></span>  | <span data-ttu-id="8286e-188">12</span><span class="sxs-lookup"><span data-stu-id="8286e-188">12</span></span>  | <span data-ttu-id="8286e-189">13</span><span class="sxs-lookup"><span data-stu-id="8286e-189">13</span></span>  | <span data-ttu-id="8286e-190">14</span><span class="sxs-lookup"><span data-stu-id="8286e-190">14</span></span>  |
| <span data-ttu-id="8286e-191">21</span><span class="sxs-lookup"><span data-stu-id="8286e-191">21</span></span>  | <span data-ttu-id="8286e-192">22</span><span class="sxs-lookup"><span data-stu-id="8286e-192">22</span></span>  | <span data-ttu-id="8286e-193">23</span><span class="sxs-lookup"><span data-stu-id="8286e-193">23</span></span>  | <span data-ttu-id="8286e-194">24</span><span class="sxs-lookup"><span data-stu-id="8286e-194">24</span></span>  |
| <span data-ttu-id="8286e-195">31</span><span class="sxs-lookup"><span data-stu-id="8286e-195">31</span></span>  | <span data-ttu-id="8286e-196">32</span><span class="sxs-lookup"><span data-stu-id="8286e-196">32</span></span>  | <span data-ttu-id="8286e-197">33</span><span class="sxs-lookup"><span data-stu-id="8286e-197">33</span></span>  | <span data-ttu-id="8286e-198">34</span><span class="sxs-lookup"><span data-stu-id="8286e-198">34</span></span>  |
| <span data-ttu-id="8286e-199">41</span><span class="sxs-lookup"><span data-stu-id="8286e-199">41</span></span>  | <span data-ttu-id="8286e-200">42</span><span class="sxs-lookup"><span data-stu-id="8286e-200">42</span></span>  | <span data-ttu-id="8286e-201">43</span><span class="sxs-lookup"><span data-stu-id="8286e-201">43</span></span>  | <span data-ttu-id="8286e-202">44</span><span class="sxs-lookup"><span data-stu-id="8286e-202">44</span></span>  |



 

<span data-ttu-id="8286e-203">Une matrice de colonne principale est présentée comme suit :</span><span class="sxs-lookup"><span data-stu-id="8286e-203">A column-major matrix is laid out like the following:</span></span>



|     |     |     |     |
|-----|-----|-----|-----|
| <span data-ttu-id="8286e-204">11</span><span class="sxs-lookup"><span data-stu-id="8286e-204">11</span></span>  | <span data-ttu-id="8286e-205">21</span><span class="sxs-lookup"><span data-stu-id="8286e-205">21</span></span>  | <span data-ttu-id="8286e-206">31</span><span class="sxs-lookup"><span data-stu-id="8286e-206">31</span></span>  | <span data-ttu-id="8286e-207">41</span><span class="sxs-lookup"><span data-stu-id="8286e-207">41</span></span>  |
| <span data-ttu-id="8286e-208">12</span><span class="sxs-lookup"><span data-stu-id="8286e-208">12</span></span>  | <span data-ttu-id="8286e-209">22</span><span class="sxs-lookup"><span data-stu-id="8286e-209">22</span></span>  | <span data-ttu-id="8286e-210">32</span><span class="sxs-lookup"><span data-stu-id="8286e-210">32</span></span>  | <span data-ttu-id="8286e-211">42</span><span class="sxs-lookup"><span data-stu-id="8286e-211">42</span></span>  |
| <span data-ttu-id="8286e-212">13</span><span class="sxs-lookup"><span data-stu-id="8286e-212">13</span></span>  | <span data-ttu-id="8286e-213">23</span><span class="sxs-lookup"><span data-stu-id="8286e-213">23</span></span>  | <span data-ttu-id="8286e-214">33</span><span class="sxs-lookup"><span data-stu-id="8286e-214">33</span></span>  | <span data-ttu-id="8286e-215">43</span><span class="sxs-lookup"><span data-stu-id="8286e-215">43</span></span>  |
| <span data-ttu-id="8286e-216">14</span><span class="sxs-lookup"><span data-stu-id="8286e-216">14</span></span>  | <span data-ttu-id="8286e-217">24</span><span class="sxs-lookup"><span data-stu-id="8286e-217">24</span></span>  | <span data-ttu-id="8286e-218">34</span><span class="sxs-lookup"><span data-stu-id="8286e-218">34</span></span>  | <span data-ttu-id="8286e-219">44</span><span class="sxs-lookup"><span data-stu-id="8286e-219">44</span></span>  |



 

<span data-ttu-id="8286e-220">Le classement des matrices de lignes et de colonnes principales détermine l’ordre dans lequel les composants de matrice sont lus à partir des entrées de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8286e-220">Row-major and column-major matrix ordering determine the order the matrix components are read from shader inputs.</span></span> <span data-ttu-id="8286e-221">Une fois les données écrites dans des registres constants, l’ordre de la matrice n’a aucun effet sur la façon dont les données sont utilisées ou accessibles à partir du code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8286e-221">Once the data is written into constant registers, matrix order has no effect on how the data is used or accessed from within shader code.</span></span> <span data-ttu-id="8286e-222">En outre, les matrices déclarées dans un corps de nuanceur ne sont pas empaquetées dans des registres constants.</span><span class="sxs-lookup"><span data-stu-id="8286e-222">Also, matrices declared in a shader body do not get packed into constant registers.</span></span> <span data-ttu-id="8286e-223">Les commandes de compression de ligne-principale et de colonne-principal n’ont aucune incidence sur l’ordre de compression des constructeurs (qui suit toujours le classement de ligne par ligne).</span><span class="sxs-lookup"><span data-stu-id="8286e-223">Row-major and column-major packing order has no influence on the packing order of constructors (which always follows row-major ordering).</span></span>

<span data-ttu-id="8286e-224">L’ordre des données dans une matrice peut être déclaré au moment de la compilation ou le compilateur classe les données au moment de l’exécution pour l’utilisation la plus efficace.</span><span class="sxs-lookup"><span data-stu-id="8286e-224">The order of the data in a matrix can be declared at compile time or the compiler will order the data at runtime for the most efficient use.</span></span>

## <a name="examples"></a><span data-ttu-id="8286e-225">Exemples</span><span class="sxs-lookup"><span data-stu-id="8286e-225">Examples</span></span>

<span data-ttu-id="8286e-226">Le langage HLSL utilise deux types spéciaux, un type de vecteur et un type de matrice pour faciliter la programmation de graphiques 2D et 3D.</span><span class="sxs-lookup"><span data-stu-id="8286e-226">HLSL uses two special types, a vector type and a matrix type to make programming 2D and 3D graphics easier.</span></span> <span data-ttu-id="8286e-227">Chacun de ces types contient plus d’un composant ; un vecteur contient jusqu’à quatre composants et une matrice contient jusqu’à 16 composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-227">Each of these types contain more than one component; a vector contains up to four components, and a matrix contains up to 16 components.</span></span> <span data-ttu-id="8286e-228">Lorsque des vecteurs et des matrices sont utilisés dans des équations HLSL standard, le calcul mathématique est conçu pour fonctionner par composant.</span><span class="sxs-lookup"><span data-stu-id="8286e-228">When vectors and matrices are used in standard HLSL equations, the math performed is designed to work per-component.</span></span> <span data-ttu-id="8286e-229">Par exemple, HLSL implémente cette multiplication :</span><span class="sxs-lookup"><span data-stu-id="8286e-229">For instance, HLSL implements this multiply:</span></span>


```
float4 v = a*b;
```



<span data-ttu-id="8286e-230">en tant que multiplication à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-230">as a four-component multiply.</span></span> <span data-ttu-id="8286e-231">Le résultat est quatre scalaires :</span><span class="sxs-lookup"><span data-stu-id="8286e-231">The result is four scalars:</span></span>


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



<span data-ttu-id="8286e-232">Il s’agit de quatre multiplicités où chaque résultat est stocké dans un composant séparé de v.</span><span class="sxs-lookup"><span data-stu-id="8286e-232">This is four multiplications where each result is stored in a separate component of v.</span></span> <span data-ttu-id="8286e-233">C’est ce qu’on appelle une multiplication à quatre composants.</span><span class="sxs-lookup"><span data-stu-id="8286e-233">This is called a four-component multiply.</span></span> <span data-ttu-id="8286e-234">Le langage HLSL utilise des mathématiques de composant qui rendent l’écriture des nuanceurs très efficace.</span><span class="sxs-lookup"><span data-stu-id="8286e-234">HLSL uses component math which makes writing shaders very efficient.</span></span>

<span data-ttu-id="8286e-235">Cela est très différent d’une multiplication qui est généralement implémentée comme un produit scalaire qui génère une seule scalaire :</span><span class="sxs-lookup"><span data-stu-id="8286e-235">This is very different from a multiply which is typically implemented as a dot product which generates a single scalar:</span></span>


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



<span data-ttu-id="8286e-236">Une matrice utilise également des opérations par composant en HLSL :</span><span class="sxs-lookup"><span data-stu-id="8286e-236">A matrix also uses per-component operations in HLSL:</span></span>


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



<span data-ttu-id="8286e-237">Le résultat est une multiplication par composant des deux matrices (par opposition à une matrice de matrice 3x3 standard).</span><span class="sxs-lookup"><span data-stu-id="8286e-237">The result is a per-component multiply of the two matrices (as opposed to a standard 3x3 matrix multiply).</span></span> <span data-ttu-id="8286e-238">Une multiplication par matrice de composant produit ce premier terme :</span><span class="sxs-lookup"><span data-stu-id="8286e-238">A per component matrix multiply yields this first term:</span></span>


```
mat3.m00 = mat1.m00 * mat2._m00;
```



<span data-ttu-id="8286e-239">Cela est différent d’une multiplication de matrice 3x3 qui produit ce premier terme :</span><span class="sxs-lookup"><span data-stu-id="8286e-239">This is different from a 3x3 matrix multiply which would yield this first term:</span></span>


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



<span data-ttu-id="8286e-240">Les versions surchargées des fonctions intrinsèques de multiplication gèrent les cas où un opérande est un vecteur et l’autre opérande est une matrice.</span><span class="sxs-lookup"><span data-stu-id="8286e-240">Overloaded versions of the multiply intrinsic function handle cases where one operand is a vector and the other operand is a matrix.</span></span> <span data-ttu-id="8286e-241">Par exemple : \* Vector Vector, vector \* Matrix, Matrix \* Vector et Matrix Matrix \* .</span><span class="sxs-lookup"><span data-stu-id="8286e-241">Such as: vector \* vector, vector \* matrix, matrix \* vector, and matrix \* matrix.</span></span> <span data-ttu-id="8286e-242">Exemple :</span><span class="sxs-lookup"><span data-stu-id="8286e-242">For instance:</span></span>


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



<span data-ttu-id="8286e-243">produit le même résultat que :</span><span class="sxs-lookup"><span data-stu-id="8286e-243">produces the same result as:</span></span>


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



<span data-ttu-id="8286e-244">Cet exemple convertit le vecteur POS en un vecteur de colonne à l’aide du cast (float1x4).</span><span class="sxs-lookup"><span data-stu-id="8286e-244">This example casts the pos vector to a column vector using the (float1x4) cast.</span></span> <span data-ttu-id="8286e-245">La modification d’un vecteur par cast ou l’échange de l’ordre des arguments fournis à Multiply équivaut à transposer la matrice.</span><span class="sxs-lookup"><span data-stu-id="8286e-245">Changing a vector by casting, or swapping the order of the arguments supplied to multiply is equivalent to transposing the matrix.</span></span>

<span data-ttu-id="8286e-246">La conversion de cast automatique fait que les fonctions de multiplication et de point intrinsèques renvoient les mêmes résultats que ceux utilisés ici :</span><span class="sxs-lookup"><span data-stu-id="8286e-246">Automatic cast conversion causes the multiply and dot intrinsic functions to return the same results as used here:</span></span>


```
{
  float4 val;
  return mul(val,val);
}
```



<span data-ttu-id="8286e-247">Le résultat de la multiplication est un \* vecteur 1x4 4x1 = 1x1.</span><span class="sxs-lookup"><span data-stu-id="8286e-247">This result of the multiply is a 1x4 \* 4x1 = 1x1 vector.</span></span> <span data-ttu-id="8286e-248">Cela équivaut à un produit scalaire :</span><span class="sxs-lookup"><span data-stu-id="8286e-248">This is equivalent to a dot product:</span></span>


```
{
  float4 val;
  return dot(val,val);
}
```



<span data-ttu-id="8286e-249">qui retourne une valeur scalaire unique.</span><span class="sxs-lookup"><span data-stu-id="8286e-249">which returns a single scalar value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8286e-250">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8286e-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8286e-251">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8286e-251">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




