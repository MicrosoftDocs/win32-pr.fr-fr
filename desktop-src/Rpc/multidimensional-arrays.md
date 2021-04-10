---
title: Tableaux multidimensionnels
description: Les attributs de tableau peuvent également être utilisés avec des tableaux multidimensionnels.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941209"
---
# <a name="multidimensional-arrays"></a><span data-ttu-id="f9a8e-103">Tableaux multidimensionnels</span><span class="sxs-lookup"><span data-stu-id="f9a8e-103">Multidimensional Arrays</span></span>

<span data-ttu-id="f9a8e-104">Les attributs de tableau peuvent également être utilisés avec des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-104">Array attributes can also be used with multidimensional arrays.</span></span> <span data-ttu-id="f9a8e-105">Toutefois, veillez à ce que chaque dimension du tableau ait un attribut correspondant.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-105">However, be careful to ensure that every dimension of the array has a corresponding attribute.</span></span> <span data-ttu-id="f9a8e-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f9a8e-106">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

<span data-ttu-id="f9a8e-107">Le tableau précédent est un tableau conforme (de taille d1size) de 30 tableaux d’éléments (avec les éléments d2len fournis pour chaque).</span><span class="sxs-lookup"><span data-stu-id="f9a8e-107">The preceding array is a conformant array (of size d1size ) of 30 element arrays (with d2len elements shipped for each).</span></span> <span data-ttu-id="f9a8e-108">La virgule entre les parenthèses de la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut spécifie que la valeur de d1size est appliquée à la première dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-108">The comma in the parentheses of the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute specifies that value in d1size is applied to the first dimension of the array.</span></span> <span data-ttu-id="f9a8e-109">De même, la commande entre les parenthèses de la \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute indique que la valeur de d2len est appliquée à la deuxième dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-109">Likewise, the command in the parentheses of the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute indicates that the value in d2len is applied to the second dimension of the array.</span></span>

<span data-ttu-id="f9a8e-110">Le compilateur MIDL 2,0 fournit deux méthodes pour marshaler des paramètres : mode mixte (/OS) et entièrement interprété (**/de l'** environnement **d’exploitation** ou/**Oicf**).</span><span class="sxs-lookup"><span data-stu-id="f9a8e-110">The MIDL 2.0 compiler provides two methods for marshaling parameters: mixed-mode (/**Os**) and fully-interpreted (/**Oif** or /**Oicf**).</span></span> <span data-ttu-id="f9a8e-111">Par défaut, le compilateur MIDL compile les interfaces en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-111">By default, the MIDL compiler compiles interfaces in mixed mode.</span></span> <span data-ttu-id="f9a8e-112">Vous n’avez pas besoin de spécifier explicitement le commutateur [**/OS**](/windows/desktop/Midl/-os) pour accéder au marshaling en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-112">You do not need to explicitly specify the [**/Os**](/windows/desktop/Midl/-os) switch to get mixed-mode marshaling.</span></span>

<span data-ttu-id="f9a8e-113">La méthode entièrement interprétée marshale les données complètement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-113">The fully-interpreted method marshals data completely offline.</span></span> <span data-ttu-id="f9a8e-114">Cela réduit considérablement la taille du code stub, mais entraîne également une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-114">This reduces the size of the stub code considerably, but it also results in decreased performance.</span></span> <span data-ttu-id="f9a8e-115">Dans le marshaling en mode mixte, les stubs marshalent certains paramètres en ligne.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-115">In mixed-mode marshaling, the stubs marshals some parameters online.</span></span> <span data-ttu-id="f9a8e-116">Bien que cela entraîne une plus grande taille de stub, elle offre également des performances accrues.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-116">While this results in a larger stub size, it also offers increased performance.</span></span>

> [!Caution]  
> <span data-ttu-id="f9a8e-117">Soyez prudent lors de la compilation des fichiers IDL dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-117">Exercise caution when compiling IDL files in this mode.</span></span> <span data-ttu-id="f9a8e-118">L’utilisation de tableaux multidimensionnels en mode mixte peut entraîner des paramètres qui ne sont pas correctement marshalés.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-118">Using multidimensional arrays in mixed mode can result in parameters that are not marshaled correctly.</span></span> <span data-ttu-id="f9a8e-119">Le commutateur de ligne de commande [**/Oicf**](/windows/desktop/Midl/-oi) est recommandé quand votre interface définit des paramètres qui sont des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-119">The [**/Oicf**](/windows/desktop/Midl/-oi) command line switch is recommended when your interface defines parameters that are multidimensional arrays.</span></span>

 

<span data-ttu-id="f9a8e-120">L' \[ [](/windows/desktop/Midl/string) \] attribut de chaîne peut également être utilisé avec des tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-120">The \[[**string**](/windows/desktop/Midl/string)\] attribute can also be used with multidimensional arrays.</span></span> <span data-ttu-id="f9a8e-121">L’attribut s’applique à la dimension la moins significative, telle qu’un tableau de chaînes conforme.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-121">The attribute applies to the least significant dimension, such as a conformant array of strings.</span></span> <span data-ttu-id="f9a8e-122">Vous pouvez également utiliser des attributs de pointeur multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-122">You can also use multidimensional pointer attributes.</span></span> <span data-ttu-id="f9a8e-123">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f9a8e-123">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

<span data-ttu-id="f9a8e-124">Dans l’exemple précédent, la variable ptr2d est un pointeur vers un bloc de pointeurs d1len, dont chacun pointe vers des pointeurs d2len vers **long**.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-124">In the preceding example, the variable ptr2d is a pointer to a d1len-sized block of pointers, each of which points to d2len pointers to **long**.</span></span>

<span data-ttu-id="f9a8e-125">Les tableaux multidimensionnels ne sont pas équivalents aux tableaux de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-125">Multidimensional arrays are not equivalent to arrays of pointers.</span></span> <span data-ttu-id="f9a8e-126">Un tableau multidimensionnel est un bloc de données unique et volumineux en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-126">A multidimensional array is a single, large block of data in memory.</span></span> <span data-ttu-id="f9a8e-127">Un tableau de pointeurs contient uniquement un bloc de pointeurs dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-127">An array of pointers only contains a block of pointers in the array.</span></span> <span data-ttu-id="f9a8e-128">Les données vers lesquelles pointent les pointeurs peuvent se trouver n’importe où dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-128">The data that the pointers point to can be anywhere in memory.</span></span> <span data-ttu-id="f9a8e-129">En outre, la syntaxe C ANSI permet de ne pas spécifier la dimension de tableau la plus significative (la plus à gauche) dans un tableau multidimensionnel.</span><span class="sxs-lookup"><span data-stu-id="f9a8e-129">Also, ANSI C syntax allows only the most significant (leftmost) array dimension to be unspecified in a multidimensional array.</span></span> <span data-ttu-id="f9a8e-130">Par conséquent, voici une instruction valide :</span><span class="sxs-lookup"><span data-stu-id="f9a8e-130">Therefore, the following is a valid statement:</span></span>

`long a1[] [20]`

<span data-ttu-id="f9a8e-131">Comparez ceci à l’instruction non valide suivante :</span><span class="sxs-lookup"><span data-stu-id="f9a8e-131">Compare this to the following invalid statement:</span></span>

`long a1[20] []`

 

 