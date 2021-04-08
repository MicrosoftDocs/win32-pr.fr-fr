---
title: C-problèmes de compression du compilateur
description: Les niveaux de compression affectent la disposition de la mémoire des types pour MIDL et le compilateur Microsoft C/C++ de la même façon.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- MIDL du compilateur MIDL, problèmes d’empaquetage du compilateur C
- compression MIDL
- configuration de la mémoire (MIDL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842225"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="88e15-106">C-problèmes de compression du compilateur</span><span class="sxs-lookup"><span data-stu-id="88e15-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="88e15-107">Les niveaux de compression affectent la disposition de la mémoire des types pour MIDL et le compilateur Microsoft C/C++ de la même façon.</span><span class="sxs-lookup"><span data-stu-id="88e15-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="88e15-108">Dans les environnements de génération Microsoft, tels que l’environnement de génération défini par VC + + ou le kit de développement logiciel (SDK) de plateforme, le niveau de compression par défaut pour les compilateurs MIDL et C/C++ est le même ; le niveau de compression par défaut pour les environnements de génération Windows 32 bits et 64 bits est 8.</span><span class="sxs-lookup"><span data-stu-id="88e15-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="88e15-109">Alignement naturel</span><span class="sxs-lookup"><span data-stu-id="88e15-109">Natural Alignment</span></span>

<span data-ttu-id="88e15-110">Pour les types en mémoire, l’alignement par défaut est identique à son alignement naturel.</span><span class="sxs-lookup"><span data-stu-id="88e15-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="88e15-111">Un type de base, tel que Short, float et \_ \_ Int64, et un pointeur sont alignés naturellement si sa représentation commence à une adresse qui est modulo sa taille.</span><span class="sxs-lookup"><span data-stu-id="88e15-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="88e15-112">Tous les types de base actuellement pris en charge ont des tailles de 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="88e15-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="88e15-113">Les pointeurs ont une taille de 4 dans les environnements 32 bits et 8 dans les environnements 64 bits.</span><span class="sxs-lookup"><span data-stu-id="88e15-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="88e15-114">Un type composé est aligné naturellement si chacun de ses composants est aligné naturellement par rapport au début du type, et s’il n’y a pas d’écarts inutiles (remplissage) entre les composants.</span><span class="sxs-lookup"><span data-stu-id="88e15-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="88e15-115">Les composants composés, tels que les champs ou les éléments, sont récursifs pour les composants de type pointeur ou de base.</span><span class="sxs-lookup"><span data-stu-id="88e15-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="88e15-116">Une règle simple pour vous aider à mémoriser ce comportement est que l’alignement naturel d’un type est égal aux alignements les plus importants de ses composants.</span><span class="sxs-lookup"><span data-stu-id="88e15-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="88e15-117">Il existe une connexion entre l’alignement et la taille de la mémoire d’un type dans des langages tels que C ou C++ et IDL, comme exprimé par l’opérateur **sizeof ()**.</span><span class="sxs-lookup"><span data-stu-id="88e15-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="88e15-118">La taille est un multiple de l’alignement (le multiple minimal qui couvre le type).</span><span class="sxs-lookup"><span data-stu-id="88e15-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="88e15-119">Cela suit à partir d’une représentation sous forme de tableau dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="88e15-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="88e15-120">L’alignement naturel est important car l’accès aux données mal alignées peut provoquer une exception sur certains systèmes.</span><span class="sxs-lookup"><span data-stu-id="88e15-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="88e15-121">Les données peuvent être marquées pour une manipulation sécurisée lorsqu’elles sont mal alignées, mais cela implique généralement une pénalité de vitesse qui peut être importante sur certaines plateformes.</span><span class="sxs-lookup"><span data-stu-id="88e15-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="88e15-122">En mémoire, les objets de types avec un alignement naturel de *n* sont garantis correctement alignés lorsqu’ils sont placés à des adresses qui sont un multiple de *n*.</span><span class="sxs-lookup"><span data-stu-id="88e15-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="88e15-123">Compression et alignement</span><span class="sxs-lookup"><span data-stu-id="88e15-123">Packing versus Alignment</span></span>

<span data-ttu-id="88e15-124">La spécification d’un niveau de compactage supérieur à l’alignement naturel d’un type ne change pas l’alignement du type.</span><span class="sxs-lookup"><span data-stu-id="88e15-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="88e15-125">La spécification d’un niveau de compactage plus petit que l’alignement naturel réduit l’alignement du type au niveau de la compression.</span><span class="sxs-lookup"><span data-stu-id="88e15-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="88e15-126">Par conséquent, les types compressés peuvent être placés en mémoire sur des adresses qui sont un multiple du niveau de compression (alignement réduit) sans entraîner de mauvais alignement.</span><span class="sxs-lookup"><span data-stu-id="88e15-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="88e15-127">Cela affecte à la fois les types simples et les types de composants.</span><span class="sxs-lookup"><span data-stu-id="88e15-127">This affects both simple types and component types.</span></span> <span data-ttu-id="88e15-128">Pour les types composés, la disposition interne du type peut être affectée, car l’alignement réduit des composants peut modifier la taille de la marge intérieure nécessaire à l’alignement correct des composants, réduisant ainsi la taille du type.</span><span class="sxs-lookup"><span data-stu-id="88e15-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="88e15-129">Une règle simple pour vous aider à mémoriser ce comportement est que le nouvel alignement d’un type condensé est le plus petit du niveau de compression et son alignement naturel.</span><span class="sxs-lookup"><span data-stu-id="88e15-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="88e15-130">La taille du type est un multiple du nouvel alignement.</span><span class="sxs-lookup"><span data-stu-id="88e15-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="88e15-131">L’opérateur **sizeof ()** retourne la taille réduite pour les types compressés.</span><span class="sxs-lookup"><span data-stu-id="88e15-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="88e15-132">Par exemple, avec le niveau de compression 2, un long est aligné sur 2 et peut donc être placé à toute adresse paire, non seulement aux adresses qui sont un multiple de 4 comme c’est le cas avec l’alignement naturel.</span><span class="sxs-lookup"><span data-stu-id="88e15-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="88e15-133">Une structure avec un short et un long, compressée à 2, n’a pas besoin de l’intervalle interne entre le short et le long suivant, nécessaire pour l’alignement naturel ; par conséquent, non seulement la structure est maintenant alignée sur 2, mais elle a également une taille réduite de 8 à 6.</span><span class="sxs-lookup"><span data-stu-id="88e15-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="88e15-134">Par exemple, considérez un type composé constitué d’un caractère codé sur 1 octet, d’un entier de 4 octets et d’un caractère de 1 octet :</span><span class="sxs-lookup"><span data-stu-id="88e15-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="88e15-135">Cette structure est naturellement alignée sur 4 et a une taille naturelle de 12.</span><span class="sxs-lookup"><span data-stu-id="88e15-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="88e15-136">Pour le niveau de compression 4 ou supérieur, la structure **MyStruct** est alignée sur 4 et `sizeof(struct mystructtype)` est égale à 12.</span><span class="sxs-lookup"><span data-stu-id="88e15-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="88e15-137">La structure sera mal alignée si elle se trouve en mémoire à une adresse qui n’est pas un multiple de 4.</span><span class="sxs-lookup"><span data-stu-id="88e15-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="88e15-138">Pour le niveau de compression 2, la structure est alignée sur 2 et sa taille est 8.</span><span class="sxs-lookup"><span data-stu-id="88e15-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="88e15-139">La structure compressée avec le niveau 2 sera mal alignée si elle se trouve en mémoire à une adresse qui n’est pas un multiple de 2.</span><span class="sxs-lookup"><span data-stu-id="88e15-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="88e15-140">Pour le niveau de compression 1, la structure est alignée sur 1 et sa taille est 6.</span><span class="sxs-lookup"><span data-stu-id="88e15-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="88e15-141">La structure compressée avec le niveau 1 peut être placée n’importe où sans entraîner une erreur d’alignement.</span><span class="sxs-lookup"><span data-stu-id="88e15-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e15-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="88e15-142">Related topics</span></span>

<dl> <span data-ttu-id="88e15-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="88e15-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="88e15-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="88e15-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="88e15-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="88e15-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 