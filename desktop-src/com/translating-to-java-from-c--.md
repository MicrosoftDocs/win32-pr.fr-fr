---
title: Conversion en Java à partir de C++
description: À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière. Les pointeurs de mémoire fournissent cet accès direct. En Java, les pointeurs sont gérés pour vous.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379655"
---
# <a name="translating-to-java-from-c"></a><span data-ttu-id="497af-105">Conversion en Java à partir de C++</span><span class="sxs-lookup"><span data-stu-id="497af-105">Translating to Java from C++</span></span>

<span data-ttu-id="497af-106">À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière.</span><span class="sxs-lookup"><span data-stu-id="497af-106">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="497af-107">Les pointeurs de mémoire fournissent cet accès direct.</span><span class="sxs-lookup"><span data-stu-id="497af-107">Memory pointers provide this direct access.</span></span> <span data-ttu-id="497af-108">En Java, les pointeurs sont gérés pour vous.</span><span class="sxs-lookup"><span data-stu-id="497af-108">In Java, pointers are handled for you.</span></span>

<span data-ttu-id="497af-109">En Java, les types de données composites **struct**, **Union** et **typedef** sont gérés exclusivement par le biais de l’utilisation de classes.</span><span class="sxs-lookup"><span data-stu-id="497af-109">In Java, **struct**, **union**, and **typedef** composite data types are handled exclusively through the use of classes.</span></span> <span data-ttu-id="497af-110">Par exemple, le type de données **Variant** C++ est mappé à **com. ms. com. variant** dans Java.</span><span class="sxs-lookup"><span data-stu-id="497af-110">For example, the C++ **VARIANT** data type maps to **com.ms.com.Variant** in Java.</span></span>

<span data-ttu-id="497af-111">En C++, les chaînes sont un tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="497af-111">In C++, strings are an array of characters.</span></span> <span data-ttu-id="497af-112">En Java, les chaînes sont des objets.</span><span class="sxs-lookup"><span data-stu-id="497af-112">In Java, strings are objects.</span></span> <span data-ttu-id="497af-113">Les méthodes qui agissent sur les chaînes traitent la chaîne comme un objet complet.</span><span class="sxs-lookup"><span data-stu-id="497af-113">Methods that act on strings treat the string as a complete object.</span></span>

<span data-ttu-id="497af-114">Les méthodes COM retournent une valeur connue sous le nom de **HRESULT**, qui est un code d’erreur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="497af-114">COM methods return a value known as a **HRESULT**, which is a 32-bit error code.</span></span> <span data-ttu-id="497af-115">La prise en charge de Java pour Microsoft Internet Explorer définit une classe, **com. ms. com. COMException**, qui encapsule le code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="497af-115">The Java support for Microsoft Internet Explorer defines a class, **com.ms.com.ComException**, which wraps the **HRESULT** error code.</span></span>

<span data-ttu-id="497af-116">Java ne prend pas en charge les types de données non signés, à l’exception de **char**, qui est un entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="497af-116">Java does not support unsigned data types except for **char**, which is a 16-bit unsigned integer.</span></span> <span data-ttu-id="497af-117">Les méthodes qui acceptent ou retournent d’autres types de données non signés ne peuvent pas être utilisées à partir de Java.</span><span class="sxs-lookup"><span data-stu-id="497af-117">Methods that accept or return other unsigned data types cannot be used from Java.</span></span>

<span data-ttu-id="497af-118">Java ne prend pas en charge les tableaux multidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="497af-118">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="497af-119">Les méthodes qui acceptent ou retournent des tableaux multidimensionnels ne sont pas disponibles à partir de Java.</span><span class="sxs-lookup"><span data-stu-id="497af-119">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="497af-120">Les valeurs booléennes dans Java ne peuvent pas être converties en 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="497af-120">Boolean values in Java cannot be cast to 0 and 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="497af-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="497af-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="497af-122">Conversion en Java</span><span class="sxs-lookup"><span data-stu-id="497af-122">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




