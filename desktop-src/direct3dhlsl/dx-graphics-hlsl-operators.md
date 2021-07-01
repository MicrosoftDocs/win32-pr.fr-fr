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
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119604"
---
# <a name="operators"></a>Opérateurs

Les expressions sont des séquences de [variables](dx-graphics-hlsl-variable-syntax.md) et de littéraux qui sont ponctuées par des [opérateurs](dx-graphics-hlsl-statement-blocks.md). Les opérateurs déterminent la façon dont les variables et les littéraux sont combinés, comparés, sélectionnés, etc. Les opérateurs sont les suivants :



| Nom de l'opérateur                                                                                | Opérateurs                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Opérateurs d’addition et de multiplication](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [Array, opérateur](#array-operator)                                               | \[i\]                                                              |
| [Opérateurs d’assignation](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [Casts binaires](#binary-casts)                                                   | Règles c pour les valeurs float et int, C ou intrinsèques HLSL pour bool     |
| [Opérateurs au niveau du bit](#bitwise-operators)                                         | ~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ = |
| [Opérateurs mathématiques booléens](#boolean-math-operators)                               | & &, \| \| , ?:                                                      |
| [Cast, opérateur](#cast-operator)                                                 | entrer                                                             |
| [Virgule (opérateur)](#comma-operator)                                               | ,                                                                  |
| [Opérateurs de comparaison](#comparison-operators)                                   | <, >, = =, ! =, <=, >=                                   |
| [Opérateurs de préfixe ou de suffixe](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Structure, opérateur](#structure-operator)                                       | .                                                                  |
| [Opérateurs unaires](#unary-operators)                                             | !, -, +                                                            |



 

La plupart des opérateurs sont par composant, ce qui signifie que l’opération est effectuée indépendamment pour chaque composant de chaque variable. Par exemple, une seule variable de composant a une opération effectuée. D’un autre côté, une variable à quatre composants a quatre opérations effectuées, une pour chaque composant.

Tous les opérateurs qui effectuent une opération sur la valeur, tels que + et \* , fonctionnent par composant.

Les opérateurs de comparaison requièrent un seul composant pour fonctionner, sauf si vous utilisez la fonction [**All**](dx-graphics-hlsl-all.md) ou [**une**](dx-graphics-hlsl-any.md) fonction intrinsèque avec une variable à plusieurs composants. L’opération suivante échoue parce que l’instruction if requiert un booléen unique mais reçoit un bool4 :


```
if (A4 < B4)
```



Les opérations suivantes ont échoué :


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



Les opérateurs de cast binaires [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), etc. fonctionnent par composant, à l’exception de [**AsDouble**](asdouble.md) dont les règles spéciales sont documentées.

Les opérateurs de sélection tels que les crochets point, virgule et tableau ne fonctionnent pas par composant.

Les opérateurs de conversion modifient le nombre de composants. Les opérations de conversion suivantes illustrent leur équivalence :


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>Opérateurs d’addition et de multiplication

Les opérateurs d’addition et de multiplication sont : +,-, \* ,/,%


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



L’opérateur modulo retourne le reste d’une division. Cela produit des résultats différents lors de l’utilisation d’entiers et de nombres à virgule flottante. Les reliquats entiers qui sont fractionnaires sont tronqués.


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



L’opérateur modulo tronque un reste fractionnaire lors de l’utilisation d’entiers.


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



L’opérateur% est défini uniquement dans les cas où les deux côtés sont positifs ou si les deux côtés sont négatifs. Contrairement à C, il fonctionne également sur les types de données à virgule flottante, ainsi que sur les entiers.

## <a name="array-operator"></a>Array, opérateur

L’opérateur de sélection de membre \[ de tableau « i \] » sélectionne un ou plusieurs composants dans un tableau. Il s’agit d’un ensemble de crochets qui contiennent un index de base zéro.


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



L’opérateur Array peut également être utilisé pour accéder à un vecteur.


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



En ajoutant un index supplémentaire, l’opérateur de tableau peut également accéder à une matrice.


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



Le premier index est l’index de ligne de base zéro. Le deuxième index est l’index de colonne de base zéro.

## <a name="assignment-operators"></a>Opérateurs d'assignation

Les opérateurs d’assignation sont : =, + =,-=, \* =,/=

Des valeurs littérales peuvent être affectées aux variables :


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



Le résultat d’une opération mathématique peut également être affecté aux variables :


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



Une variable peut être utilisée de chaque côté du signe égal :


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



La Division pour les variables à virgule flottante est la même que celle attendue, car les restes décimaux ne sont pas un problème.


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



Soyez prudent si vous utilisez des entiers qui peuvent être divisés, en particulier lorsque la troncation affecte le résultat. Cet exemple est identique à l’exemple précédent, à l’exception du type de données. La troncation provoque un résultat très différent.


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>Casts binaires

L’opération de conversion entre int et float convertit la valeur numérique en représentations appropriées suivant les règles C pour tronquer un type int. Le fait d’effectuer un cast d’une valeur d’un float vers un int et de revenir à un float entraîne une conversion avec perte en fonction de la précision de la cible.

Les casts binaires peuvent également être effectués à l’aide de [**fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)qui réinterprètent la représentation de bits d’un nombre dans le type de données cible.


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>Opérateurs au niveau du bit

Le langage HLSL prend en charge les opérateurs de bits suivants, qui suivent la même priorité que C en ce qui concerne les autres opérateurs. Le tableau suivant décrit les opérateurs.

> [!Note]  
> Les opérateurs au niveau du bit nécessitent le [modèle de nuanceur 4 \_ 0](dx-graphics-hlsl-sm4.md) avec Direct3D 10 et un matériel supérieur.

 



| Opérateur          |  Fonction                 |
|-----------|-------------------|
| ~         | Not logique       |
| <<  | Décalage vers la gauche        |
| >>  | Décalage vers la droite       |
| &         | AND logique       |
| \|        | Or logique        |
| ^         | XOR logique       |
| <<= | Décalage vers la gauche égal  |
| >>= | Décalage vers la droite égal |
| &=        | Et égal à         |
| \|=       | Ou égal à          |
| ^=        | XOR égal         |



 

Les opérateurs au niveau du bit sont définis pour fonctionner uniquement sur les types de données int et uint. Toute tentative d’utilisation d’opérateurs de bits sur float, ou de types de données struct, génère une erreur.

## <a name="boolean-math-operators"></a>Opérateurs mathématiques booléens

Les opérateurs mathématiques booléens sont les suivants :  &&, \| \| , ?:


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



Contrairement à l’évaluation de court-circuit de &&, \| \| et ?: en C, les expressions HLSL ne peuvent jamais court-circuiter une évaluation, car il s’agit d’opérations vectorielles. Tous les côtés de l’expression sont toujours évalués.

Les opérateurs booléens fonctionnent pour chaque composant. Cela signifie que si vous comparez deux vecteurs, le résultat est un vecteur contenant le résultat booléen de la comparaison pour chaque composant.

Pour les expressions qui utilisent des opérateurs booléens, la taille et le type de composant de chaque variable sont promus pour être identiques avant que l’opération ne se produise. Le type promu détermine la résolution à laquelle l’opération a lieu, ainsi que le type de résultat de l’expression. Par exemple, une expression Int3 + float est promue en float3 + float3 pour évaluation, et son résultat est de type float3.

## <a name="cast-operator"></a>Opérateur de conversion

Une expression précédée d’un nom de type entre parenthèses est un cast de type explicite. Une conversion de type convertit l’expression d’origine en type de données du cast. En général, les types de données simples peuvent être convertis en types de données plus complexes (avec un cast de promotion), mais seuls certains types de données complexes peuvent être converties en types de données simples (avec un cast de rétrogradation).

Seule la conversion de type de partie droite est légale. Par exemple, les expressions telles que `(int)myFloat = myInt;` ne sont pas autorisées. Utilisez `myFloat = (float)myInt;` à la place.

Le compilateur effectue également une conversion de type implicite. Par exemple, les deux expressions suivantes sont équivalentes :


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>Virgule (opérateur)

L’opérateur virgule (,) sépare une ou plusieurs expressions qui doivent être évaluées dans l’ordre. La valeur de la dernière expression dans la séquence est utilisée comme valeur de la séquence.

Voici un cas intéressant d’attirer l’attention sur. Si le type de constructeur est accidentellement quitté du côté droit du signe égal, le côté droit contient désormais quatre expressions, séparées par trois virgules.


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



L’opérateur virgule évalue une expression de gauche à droite. Cela réduit le côté droit pour :


```
float4 x = 1; 
```



Le langage HLSL utilise la promotion scalaire dans ce cas, le résultat est donc comme s’il avait été écrit comme suit :


```
float4 x = float4(1,1,1,1);
```



Dans ce cas, le fait de quitter le type float4 du côté droit est sans doute une erreur que le compilateur ne peut pas détecter, car il s’agit d’une instruction valide.

## <a name="comparison-operators"></a>Opérateurs de comparaison

Les opérateurs de comparaison sont les suivants : <, >, = =, ! =, <=, >=.

Comparez les valeurs qui sont supérieures (ou inférieures à) à toute valeur scalaire :


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



Ou comparez les valeurs égales à (ou différentes) à toute valeur scalaire :


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



Vous pouvez aussi combiner et comparer des valeurs qui sont supérieures ou égales à (ou inférieures ou égales à) à toute valeur scalaire :


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



Chacune de ces comparaisons peut être effectuée avec n’importe quel type de données scalaires.

Pour utiliser des opérateurs de comparaison avec des types de vecteurs et de matrices, utilisez la fonction [**All**](dx-graphics-hlsl-all.md) ou [**any**](dx-graphics-hlsl-any.md) intrinsèque.

Cette opération échoue parce que l’instruction if requiert un booléen unique mais reçoit un bool4 :


```
if (A4 < B4)
```



Ces opérations ont échoué :


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>Opérateurs de préfixe ou de suffixe

Les opérateurs de préfixe et de suffixe sont : + +,--. Les opérateurs de préfixe modifient le contenu de la variable avant l’évaluation de l’expression. Les opérateurs postfix modifient le contenu de la variable après l’évaluation de l’expression.

Dans ce cas, une boucle utilise le contenu de i pour suivre le nombre de boucles.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



Étant donné que l’opérateur d’incrémentation postfixé (+ +) est utilisé, arrayOfFloats \[ \] est multiplié par 2 avant d’être incrémenté. Cela peut être légèrement réorganisé pour utiliser l’opérateur d’incrément de préfixe. Celle-ci est plus difficile à lire, bien que les deux exemples soient équivalents.


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



Étant donné que l’opérateur préfixé (+ +) est utilisé, arrayOfFloats \[ i + 1-1 \] est multiplié par 2 après l’incrémentation.

L’opérateur de décrémentation préfixé et postfixé (--) sont appliqués dans la même séquence que l’opérateur d’incrémentation. La différence est que la décrémentation soustrait 1 au lieu d’ajouter 1.

## <a name="structure-operator"></a>Structure, opérateur

L’opérateur de sélection de membre de structure (.) est un point. À partir de cette structure :


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



Il peut être lu comme suit :


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



Chaque membre peut être lu ou écrit à l’aide de l’opérateur de structure :


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>Opérateurs unaires

Les opérateurs unaires sont les suivants :!,-, +

Les opérateurs unaires opèrent sur un seul opérande.


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>Priorité des opérateurs

Lorsqu’une expression contient plusieurs opérateurs, la priorité des opérateurs détermine l’ordre d’évaluation. La priorité des opérateurs pour le langage HLSL suit la même priorité que C.

## <a name="remarks"></a>Remarques

Les accolades ( {,} ) commencent et terminent un bloc d’instructions. Lorsqu’un bloc d’instructions utilise une seule instruction, les accolades sont facultatives.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions (DirectX HLSL)](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




