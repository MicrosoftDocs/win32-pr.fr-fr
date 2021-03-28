---
title: Type de matrice
description: Une matrice est un type de données spécial qui contient entre un et seize composants. Chaque composant d’une matrice doit être du même type.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Type de matrice HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030020"
---
# <a name="matrix-type"></a><span data-ttu-id="0a3ff-105">Type de matrice</span><span class="sxs-lookup"><span data-stu-id="0a3ff-105">Matrix Type</span></span>

<span data-ttu-id="0a3ff-106">Une matrice est un type de données spécial qui contient entre un et seize composants.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-106">A matrix is a special data type that contains between one and sixteen components.</span></span> <span data-ttu-id="0a3ff-107">Chaque composant d’une matrice doit être du même type.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-107">Every component of a matrix must be of the same type.</span></span>



|                         |
|-------------------------|
| <span data-ttu-id="0a3ff-108">**Nom de TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="0a3ff-108">**TypeComponents Name**</span></span> |



 

## <a name="components"></a><span data-ttu-id="0a3ff-109">Components</span><span class="sxs-lookup"><span data-stu-id="0a3ff-109">Components</span></span>



| <span data-ttu-id="0a3ff-110">Élément</span><span class="sxs-lookup"><span data-stu-id="0a3ff-110">Item</span></span>                                                                                                                             | <span data-ttu-id="0a3ff-111">Description</span><span class="sxs-lookup"><span data-stu-id="0a3ff-111">Description</span></span>                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3ff-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="0a3ff-112"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="0a3ff-113">Nom unique qui contient trois parties.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-113">A single name that contains three parts.</span></span> <span data-ttu-id="0a3ff-114">La première partie est l’un des types [scalaires](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="0a3ff-114">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="0a3ff-115">La deuxième partie est le nombre de lignes.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-115">The second part is the number of rows.</span></span> <span data-ttu-id="0a3ff-116">La troisième partie est le nombre de colonnes.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-116">The third part is the number of columns.</span></span> <span data-ttu-id="0a3ff-117">Le nombre de lignes et de colonnes est un entier positif compris entre 1 et 4 inclus.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-117">The number of rows and columns is a positive integer between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="0a3ff-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="0a3ff-118"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="0a3ff-119">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-119">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a><span data-ttu-id="0a3ff-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="0a3ff-120">Examples</span></span>

<span data-ttu-id="0a3ff-121">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="0a3ff-121">Here are some examples:</span></span>


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



<span data-ttu-id="0a3ff-122">Une matrice peut également être déclarée à l’aide de cette syntaxe :</span><span class="sxs-lookup"><span data-stu-id="0a3ff-122">A matrix can be declared using this syntax also:</span></span>


```
matrix <Type, Number> VariableName
```



<span data-ttu-id="0a3ff-123">Le type de matrice utilise les crochets angulaires pour spécifier le type, le nombre de lignes et le nombre de colonnes.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-123">The matrix type uses the angle brackets to specify the type, the number of rows, and the number of columns.</span></span> <span data-ttu-id="0a3ff-124">Cet exemple crée une matrice à virgule flottante, avec deux lignes et deux colonnes.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-124">This example creates a floating-point matrix, with two rows and two columns.</span></span> <span data-ttu-id="0a3ff-125">Tous les types de données scalaires peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="0a3ff-125">Any of the scalar data types can be used.</span></span>

<span data-ttu-id="0a3ff-126">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="0a3ff-126">Here is an example:</span></span>


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a><span data-ttu-id="0a3ff-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a3ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3ff-128">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0a3ff-128">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





