---
title: Opérateurs
description: Les expressions sont des séquences de variables et de littéraux qui sont ponctuées par des opérateurs.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2020
ms.locfileid: "104462758"
---
# <a name="operators"></a><span data-ttu-id="056b7-103">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="056b7-103">Operators</span></span>

<span data-ttu-id="056b7-104">Les expressions sont des séquences de [variables](dx-graphics-hlsl-variable-syntax.md) et de littéraux qui sont ponctuées par des [opérateurs](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="056b7-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="056b7-105">Les opérateurs déterminent la façon dont les variables et les littéraux sont combinés, comparés, sélectionnés, etc.</span><span class="sxs-lookup"><span data-stu-id="056b7-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="056b7-106">Les opérateurs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="056b7-106">The operators include:</span></span>



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="056b7-107">Nom de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-107">Operator Name</span></span>                                                                   | <span data-ttu-id="056b7-108">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="056b7-108">Operators</span></span>                                                          |
| [<span data-ttu-id="056b7-109">Opérateurs d’addition et de multiplication</span><span class="sxs-lookup"><span data-stu-id="056b7-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="056b7-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="056b7-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="056b7-111">Array, opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="056b7-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="056b7-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="056b7-113">Opérateurs d’assignation</span><span class="sxs-lookup"><span data-stu-id="056b7-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="056b7-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="056b7-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="056b7-115">Casts binaires</span><span class="sxs-lookup"><span data-stu-id="056b7-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="056b7-116">Règles c pour les valeurs float et int, C ou intrinsèques HLSL pour bool</span><span class="sxs-lookup"><span data-stu-id="056b7-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="056b7-117">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="056b7-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="056b7-118">~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ =</span><span class="sxs-lookup"><span data-stu-id="056b7-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="056b7-119">Opérateurs mathématiques booléens</span><span class="sxs-lookup"><span data-stu-id="056b7-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="056b7-120">& &, \| \| , ?:</span><span class="sxs-lookup"><span data-stu-id="056b7-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="056b7-121">Cast, opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="056b7-122">entrer</span><span class="sxs-lookup"><span data-stu-id="056b7-122">(type)</span></span>                                                             |
| [<span data-ttu-id="056b7-123">Virgule (opérateur)</span><span class="sxs-lookup"><span data-stu-id="056b7-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="056b7-124">,</span><span class="sxs-lookup"><span data-stu-id="056b7-124">,</span></span>                                                                  |
| [<span data-ttu-id="056b7-125">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="056b7-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="056b7-126"><, >, = =, ! =, <=, >=</span><span class="sxs-lookup"><span data-stu-id="056b7-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="056b7-127">Opérateurs de préfixe ou de suffixe</span><span class="sxs-lookup"><span data-stu-id="056b7-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="056b7-128">++, --</span><span class="sxs-lookup"><span data-stu-id="056b7-128">++, --</span></span>                                                             |
| [<span data-ttu-id="056b7-129">Structure, opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="056b7-130">.</span><span class="sxs-lookup"><span data-stu-id="056b7-130">.</span></span>                                                                  |
| [<span data-ttu-id="056b7-131">Opérateurs unaires</span><span class="sxs-lookup"><span data-stu-id="056b7-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="056b7-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="056b7-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="056b7-133">La plupart des opérateurs sont par composant, ce qui signifie que l’opération est effectuée indépendamment pour chaque composant de chaque variable.</span><span class="sxs-lookup"><span data-stu-id="056b7-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="056b7-134">Par exemple, une seule variable de composant a une opération effectuée.</span><span class="sxs-lookup"><span data-stu-id="056b7-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="056b7-135">D’un autre côté, une variable à quatre composants a quatre opérations effectuées, une pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="056b7-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="056b7-136">Tous les opérateurs qui effectuent une opération sur la valeur, tels que + et \* , fonctionnent par composant.</span><span class="sxs-lookup"><span data-stu-id="056b7-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="056b7-137">Les opérateurs de comparaison requièrent un seul composant pour fonctionner, sauf si vous utilisez la fonction [**All**](dx-graphics-hlsl-all.md) ou [**une**](dx-graphics-hlsl-any.md) fonction intrinsèque avec une variable à plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="056b7-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="056b7-138">L’opération suivante échoue parce que l’instruction if requiert un booléen unique mais reçoit un bool4 :</span><span class="sxs-lookup"><span data-stu-id="056b7-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="056b7-139">Les opérations suivantes ont échoué :</span><span class="sxs-lookup"><span data-stu-id="056b7-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="056b7-140">Les opérateurs de cast binaires [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), etc. fonctionnent par composant, à l’exception de [**AsDouble**](asdouble.md) dont les règles spéciales sont documentées.</span><span class="sxs-lookup"><span data-stu-id="056b7-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="056b7-141">Les opérateurs de sélection tels que les crochets point, virgule et tableau ne fonctionnent pas par composant.</span><span class="sxs-lookup"><span data-stu-id="056b7-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="056b7-142">Les opérateurs de conversion modifient le nombre de composants.</span><span class="sxs-lookup"><span data-stu-id="056b7-142">Cast operators change the number of components.</span></span> <span data-ttu-id="056b7-143">Les opérations de conversion suivantes illustrent leur équivalence :</span><span class="sxs-lookup"><span data-stu-id="056b7-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="056b7-144">Opérateurs d’addition et de multiplication</span><span class="sxs-lookup"><span data-stu-id="056b7-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="056b7-145">Les opérateurs d’addition et de multiplication sont : +,-, \* ,/,%</span><span class="sxs-lookup"><span data-stu-id="056b7-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



<span data-ttu-id="056b7-146">L’opérateur modulo retourne le reste d’une division.</span><span class="sxs-lookup"><span data-stu-id="056b7-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="056b7-147">Cela produit des résultats différents lors de l’utilisation d’entiers et de nombres à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="056b7-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="056b7-148">Les reliquats entiers qui sont fractionnaires sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="056b7-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="056b7-149">L’opérateur modulo tronque un reste fractionnaire lors de l’utilisation d’entiers.</span><span class="sxs-lookup"><span data-stu-id="056b7-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="056b7-150">L’opérateur% est défini uniquement dans les cas où les deux côtés sont positifs ou si les deux côtés sont négatifs.</span><span class="sxs-lookup"><span data-stu-id="056b7-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="056b7-151">Contrairement à C, il fonctionne également sur les types de données à virgule flottante, ainsi que sur les entiers.</span><span class="sxs-lookup"><span data-stu-id="056b7-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="056b7-152">Array, opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-152">Array Operator</span></span>

<span data-ttu-id="056b7-153">L’opérateur de sélection de membre \[ de tableau « i \] » sélectionne un ou plusieurs composants dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="056b7-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="056b7-154">Il s’agit d’un ensemble de crochets qui contiennent un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="056b7-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="056b7-155">L’opérateur Array peut également être utilisé pour accéder à un vecteur.</span><span class="sxs-lookup"><span data-stu-id="056b7-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="056b7-156">En ajoutant un index supplémentaire, l’opérateur de tableau peut également accéder à une matrice.</span><span class="sxs-lookup"><span data-stu-id="056b7-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="056b7-157">Le premier index est l’index de ligne de base zéro.</span><span class="sxs-lookup"><span data-stu-id="056b7-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="056b7-158">Le deuxième index est l’index de colonne de base zéro.</span><span class="sxs-lookup"><span data-stu-id="056b7-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="056b7-159">Opérateurs d'assignation</span><span class="sxs-lookup"><span data-stu-id="056b7-159">Assignment Operators</span></span>

<span data-ttu-id="056b7-160">Les opérateurs d’assignation sont : =, + =,-=, \* =,/=</span><span class="sxs-lookup"><span data-stu-id="056b7-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="056b7-161">Des valeurs littérales peuvent être affectées aux variables :</span><span class="sxs-lookup"><span data-stu-id="056b7-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="056b7-162">Le résultat d’une opération mathématique peut également être affecté aux variables :</span><span class="sxs-lookup"><span data-stu-id="056b7-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="056b7-163">Une variable peut être utilisée de chaque côté du signe égal :</span><span class="sxs-lookup"><span data-stu-id="056b7-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="056b7-164">La Division pour les variables à virgule flottante est la même que celle attendue, car les restes décimaux ne sont pas un problème.</span><span class="sxs-lookup"><span data-stu-id="056b7-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="056b7-165">Soyez prudent si vous utilisez des entiers qui peuvent être divisés, en particulier lorsque la troncation affecte le résultat.</span><span class="sxs-lookup"><span data-stu-id="056b7-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="056b7-166">Cet exemple est identique à l’exemple précédent, à l’exception du type de données.</span><span class="sxs-lookup"><span data-stu-id="056b7-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="056b7-167">La troncation provoque un résultat très différent.</span><span class="sxs-lookup"><span data-stu-id="056b7-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="056b7-168">Casts binaires</span><span class="sxs-lookup"><span data-stu-id="056b7-168">Binary Casts</span></span>

<span data-ttu-id="056b7-169">L’opération de conversion entre int et float convertit la valeur numérique en représentations appropriées suivant les règles C pour tronquer un type int.</span><span class="sxs-lookup"><span data-stu-id="056b7-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="056b7-170">Le fait d’effectuer un cast d’une valeur d’un float vers un int et de revenir à un float entraîne une conversion avec perte en fonction de la précision de la cible.</span><span class="sxs-lookup"><span data-stu-id="056b7-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="056b7-171">Les casts binaires peuvent également être effectués à l’aide de [**fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)qui réinterprètent la représentation de bits d’un nombre dans le type de données cible.</span><span class="sxs-lookup"><span data-stu-id="056b7-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="056b7-172">Opérateurs au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="056b7-172">Bitwise Operators</span></span>

<span data-ttu-id="056b7-173">Le langage HLSL prend en charge les opérateurs de bits suivants, qui suivent la même priorité que C en ce qui concerne les autres opérateurs.</span><span class="sxs-lookup"><span data-stu-id="056b7-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="056b7-174">Le tableau suivant décrit les opérateurs.</span><span class="sxs-lookup"><span data-stu-id="056b7-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="056b7-175">Les opérateurs au niveau du bit nécessitent le [modèle de nuanceur 4 \_ 0](dx-graphics-hlsl-sm4.md) avec Direct3D 10 et un matériel supérieur.</span><span class="sxs-lookup"><span data-stu-id="056b7-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



|           |                   |
|-----------|-------------------|
| <span data-ttu-id="056b7-176">Opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-176">Operator</span></span>  | <span data-ttu-id="056b7-177">Fonction</span><span class="sxs-lookup"><span data-stu-id="056b7-177">Function</span></span>          |
| ~         | <span data-ttu-id="056b7-178">Not logique</span><span class="sxs-lookup"><span data-stu-id="056b7-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="056b7-179">Décalage vers la gauche</span><span class="sxs-lookup"><span data-stu-id="056b7-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="056b7-180">Décalage vers la droite</span><span class="sxs-lookup"><span data-stu-id="056b7-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="056b7-181">AND logique</span><span class="sxs-lookup"><span data-stu-id="056b7-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="056b7-182">Or logique</span><span class="sxs-lookup"><span data-stu-id="056b7-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="056b7-183">XOR logique</span><span class="sxs-lookup"><span data-stu-id="056b7-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="056b7-184">Décalage vers la gauche égal</span><span class="sxs-lookup"><span data-stu-id="056b7-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="056b7-185">Décalage vers la droite égal</span><span class="sxs-lookup"><span data-stu-id="056b7-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="056b7-186">Et égal à</span><span class="sxs-lookup"><span data-stu-id="056b7-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="056b7-187">Ou égal à</span><span class="sxs-lookup"><span data-stu-id="056b7-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="056b7-188">XOR égal</span><span class="sxs-lookup"><span data-stu-id="056b7-188">Xor Equal</span></span>         |



 

<span data-ttu-id="056b7-189">Les opérateurs au niveau du bit sont définis pour fonctionner uniquement sur les types de données int et uint.</span><span class="sxs-lookup"><span data-stu-id="056b7-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="056b7-190">Toute tentative d’utilisation d’opérateurs de bits sur float, ou de types de données struct, génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="056b7-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="056b7-191">Opérateurs mathématiques booléens</span><span class="sxs-lookup"><span data-stu-id="056b7-191">Boolean Math Operators</span></span>

<span data-ttu-id="056b7-192">Les opérateurs mathématiques booléens sont les suivants :  &&, \| \| , ?:</span><span class="sxs-lookup"><span data-stu-id="056b7-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="056b7-193">Contrairement à l’évaluation de court-circuit de &&, \| \| et ?: en C, les expressions HLSL ne peuvent jamais court-circuiter une évaluation, car il s’agit d’opérations vectorielles.</span><span class="sxs-lookup"><span data-stu-id="056b7-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="056b7-194">Tous les côtés de l’expression sont toujours évalués.</span><span class="sxs-lookup"><span data-stu-id="056b7-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="056b7-195">Les opérateurs booléens fonctionnent pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="056b7-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="056b7-196">Cela signifie que si vous comparez deux vecteurs, le résultat est un vecteur contenant le résultat booléen de la comparaison pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="056b7-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="056b7-197">Pour les expressions qui utilisent des opérateurs booléens, la taille et le type de composant de chaque variable sont promus pour être identiques avant que l’opération ne se produise.</span><span class="sxs-lookup"><span data-stu-id="056b7-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="056b7-198">Le type promu détermine la résolution à laquelle l’opération a lieu, ainsi que le type de résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="056b7-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="056b7-199">Par exemple, une expression Int3 + float est promue en float3 + float3 pour évaluation, et son résultat est de type float3.</span><span class="sxs-lookup"><span data-stu-id="056b7-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="056b7-200">Opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="056b7-200">Cast Operator</span></span>

<span data-ttu-id="056b7-201">Une expression précédée d’un nom de type entre parenthèses est un cast de type explicite.</span><span class="sxs-lookup"><span data-stu-id="056b7-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="056b7-202">Une conversion de type convertit l’expression d’origine en type de données du cast.</span><span class="sxs-lookup"><span data-stu-id="056b7-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="056b7-203">En général, les types de données simples peuvent être convertis en types de données plus complexes (avec un cast de promotion), mais seuls certains types de données complexes peuvent être converties en types de données simples (avec un cast de rétrogradation).</span><span class="sxs-lookup"><span data-stu-id="056b7-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="056b7-204">Seule la conversion de type de partie droite est légale.</span><span class="sxs-lookup"><span data-stu-id="056b7-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="056b7-205">Par exemple, les expressions telles que `(int)myFloat = myInt;` ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="056b7-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="056b7-206">Utilisez `myFloat = (float)myInt;` à la place.</span><span class="sxs-lookup"><span data-stu-id="056b7-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="056b7-207">Le compilateur effectue également une conversion de type implicite.</span><span class="sxs-lookup"><span data-stu-id="056b7-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="056b7-208">Par exemple, les deux expressions suivantes sont équivalentes :</span><span class="sxs-lookup"><span data-stu-id="056b7-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="056b7-209">Virgule (opérateur)</span><span class="sxs-lookup"><span data-stu-id="056b7-209">Comma Operator</span></span>

<span data-ttu-id="056b7-210">L’opérateur virgule (,) sépare une ou plusieurs expressions qui doivent être évaluées dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="056b7-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="056b7-211">La valeur de la dernière expression dans la séquence est utilisée comme valeur de la séquence.</span><span class="sxs-lookup"><span data-stu-id="056b7-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="056b7-212">Voici un cas intéressant d’attirer l’attention sur.</span><span class="sxs-lookup"><span data-stu-id="056b7-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="056b7-213">Si le type de constructeur est accidentellement quitté du côté droit du signe égal, le côté droit contient désormais quatre expressions, séparées par trois virgules.</span><span class="sxs-lookup"><span data-stu-id="056b7-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="056b7-214">L’opérateur virgule évalue une expression de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="056b7-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="056b7-215">Cela réduit le côté droit pour :</span><span class="sxs-lookup"><span data-stu-id="056b7-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="056b7-216">Le langage HLSL utilise la promotion scalaire dans ce cas, le résultat est donc comme s’il avait été écrit comme suit :</span><span class="sxs-lookup"><span data-stu-id="056b7-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="056b7-217">Dans ce cas, le fait de quitter le type float4 du côté droit est sans doute une erreur que le compilateur ne peut pas détecter, car il s’agit d’une instruction valide.</span><span class="sxs-lookup"><span data-stu-id="056b7-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="056b7-218">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="056b7-218">Comparison Operators</span></span>

<span data-ttu-id="056b7-219">Les opérateurs de comparaison sont les suivants : <, >, = =, ! =, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="056b7-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="056b7-220">Comparez les valeurs qui sont supérieures (ou inférieures à) à toute valeur scalaire :</span><span class="sxs-lookup"><span data-stu-id="056b7-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="056b7-221">Ou comparez les valeurs égales à (ou différentes) à toute valeur scalaire :</span><span class="sxs-lookup"><span data-stu-id="056b7-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="056b7-222">Vous pouvez aussi combiner et comparer des valeurs qui sont supérieures ou égales à (ou inférieures ou égales à) à toute valeur scalaire :</span><span class="sxs-lookup"><span data-stu-id="056b7-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="056b7-223">Chacune de ces comparaisons peut être effectuée avec n’importe quel type de données scalaires.</span><span class="sxs-lookup"><span data-stu-id="056b7-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="056b7-224">Pour utiliser des opérateurs de comparaison avec des types de vecteurs et de matrices, utilisez la fonction [**All**](dx-graphics-hlsl-all.md) ou [**any**](dx-graphics-hlsl-any.md) intrinsèque.</span><span class="sxs-lookup"><span data-stu-id="056b7-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="056b7-225">Cette opération échoue parce que l’instruction if requiert un booléen unique mais reçoit un bool4 :</span><span class="sxs-lookup"><span data-stu-id="056b7-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="056b7-226">Ces opérations ont échoué :</span><span class="sxs-lookup"><span data-stu-id="056b7-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="056b7-227">Opérateurs de préfixe ou de suffixe</span><span class="sxs-lookup"><span data-stu-id="056b7-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="056b7-228">Les opérateurs de préfixe et de suffixe sont : + +,--.</span><span class="sxs-lookup"><span data-stu-id="056b7-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="056b7-229">Les opérateurs de préfixe modifient le contenu de la variable avant l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="056b7-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="056b7-230">Les opérateurs postfix modifient le contenu de la variable après l’évaluation de l’expression.</span><span class="sxs-lookup"><span data-stu-id="056b7-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="056b7-231">Dans ce cas, une boucle utilise le contenu de i pour suivre le nombre de boucles.</span><span class="sxs-lookup"><span data-stu-id="056b7-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="056b7-232">Étant donné que l’opérateur d’incrémentation postfixé (+ +) est utilisé, arrayOfFloats \[ \] est multiplié par 2 avant d’être incrémenté.</span><span class="sxs-lookup"><span data-stu-id="056b7-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="056b7-233">Cela peut être légèrement réorganisé pour utiliser l’opérateur d’incrément de préfixe.</span><span class="sxs-lookup"><span data-stu-id="056b7-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="056b7-234">Celle-ci est plus difficile à lire, bien que les deux exemples soient équivalents.</span><span class="sxs-lookup"><span data-stu-id="056b7-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="056b7-235">Étant donné que l’opérateur préfixé (+ +) est utilisé, arrayOfFloats \[ i + 1-1 \] est multiplié par 2 après l’incrémentation.</span><span class="sxs-lookup"><span data-stu-id="056b7-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="056b7-236">L’opérateur de décrémentation préfixé et postfixé (--) sont appliqués dans la même séquence que l’opérateur d’incrémentation.</span><span class="sxs-lookup"><span data-stu-id="056b7-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="056b7-237">La différence est que la décrémentation soustrait 1 au lieu d’ajouter 1.</span><span class="sxs-lookup"><span data-stu-id="056b7-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="056b7-238">Structure, opérateur</span><span class="sxs-lookup"><span data-stu-id="056b7-238">Structure Operator</span></span>

<span data-ttu-id="056b7-239">L’opérateur de sélection de membre de structure (.) est un point.</span><span class="sxs-lookup"><span data-stu-id="056b7-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="056b7-240">À partir de cette structure :</span><span class="sxs-lookup"><span data-stu-id="056b7-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="056b7-241">Il peut être lu comme suit :</span><span class="sxs-lookup"><span data-stu-id="056b7-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="056b7-242">Chaque membre peut être lu ou écrit à l’aide de l’opérateur de structure :</span><span class="sxs-lookup"><span data-stu-id="056b7-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="056b7-243">Opérateurs unaires</span><span class="sxs-lookup"><span data-stu-id="056b7-243">Unary Operators</span></span>

<span data-ttu-id="056b7-244">Les opérateurs unaires sont les suivants :!,-, +</span><span class="sxs-lookup"><span data-stu-id="056b7-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="056b7-245">Les opérateurs unaires opèrent sur un seul opérande.</span><span class="sxs-lookup"><span data-stu-id="056b7-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="056b7-246">Priorité des opérateurs</span><span class="sxs-lookup"><span data-stu-id="056b7-246">Operator Precedence</span></span>

<span data-ttu-id="056b7-247">Lorsqu’une expression contient plusieurs opérateurs, la priorité des opérateurs détermine l’ordre d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="056b7-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="056b7-248">La priorité des opérateurs pour le langage HLSL suit la même priorité que C.</span><span class="sxs-lookup"><span data-stu-id="056b7-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="056b7-249">Notes</span><span class="sxs-lookup"><span data-stu-id="056b7-249">Remarks</span></span>

<span data-ttu-id="056b7-250">Les accolades ( {,} ) commencent et terminent un bloc d’instructions.</span><span class="sxs-lookup"><span data-stu-id="056b7-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="056b7-251">Lorsqu’un bloc d’instructions utilise une seule instruction, les accolades sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="056b7-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="056b7-252">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="056b7-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="056b7-253">Instructions (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="056b7-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




