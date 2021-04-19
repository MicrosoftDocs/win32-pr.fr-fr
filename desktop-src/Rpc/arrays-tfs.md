---
title: Tableaux (RPC) (TFS)
description: Les catégories de tableau de l’appel de procédure distante (RPC) incluent des catégories de taille fixe, de conformité et de variation, variables et complexes.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106531178"
---
# <a name="arrays-rpc"></a><span data-ttu-id="d4d7b-103">Tableaux (RPC)</span><span class="sxs-lookup"><span data-stu-id="d4d7b-103">Arrays (RPC)</span></span>

<span data-ttu-id="d4d7b-104">Plusieurs catégories de tableaux ont été définies en fonction de leurs caractéristiques de performances, en particulier si le tableau peut être copié par bloc.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="d4d7b-105">Pour certaines catégories, telles qu’un tableau de taille fixe, il existe deux types de descripteurs de tableau ; ils sont indiqués par un correctif dans le nom du jeton FC de début.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="d4d7b-106">Caractère de format</span><span class="sxs-lookup"><span data-stu-id="d4d7b-106">Format character</span></span> | <span data-ttu-id="d4d7b-107">Description</span><span class="sxs-lookup"><span data-stu-id="d4d7b-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="d4d7b-108">SM</span><span class="sxs-lookup"><span data-stu-id="d4d7b-108">SM</span></span>               | <span data-ttu-id="d4d7b-109">La taille totale du type peut être représentée dans un entier non signé 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="d4d7b-110">LG</span><span class="sxs-lookup"><span data-stu-id="d4d7b-110">LG</span></span>               | <span data-ttu-id="d4d7b-111">La taille totale du type a besoin d’un long non signé 32 bits pour être représenté.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="d4d7b-112">Champs communs aux tableaux :</span><span class="sxs-lookup"><span data-stu-id="d4d7b-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="d4d7b-113">\_taille totale</span><span class="sxs-lookup"><span data-stu-id="d4d7b-113">total\_size</span></span>

    <span data-ttu-id="d4d7b-114">Taille totale du tableau en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="d4d7b-115">Cela est identique à la taille du câble après l’alignement.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="d4d7b-116">La taille totale est calculée pour les catégories pour lesquelles le problème de remplissage n’existe pas et la taille correspond à la taille réelle du tableau.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="d4d7b-117">taille de l’élément \_</span><span class="sxs-lookup"><span data-stu-id="d4d7b-117">element\_size</span></span>

    <span data-ttu-id="d4d7b-118">Taille totale en mémoire d’un seul élément du tableau, y compris le remplissage (cela peut se produire pour les tableaux complexes uniquement).</span><span class="sxs-lookup"><span data-stu-id="d4d7b-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="d4d7b-119">Description de l’élément \_</span><span class="sxs-lookup"><span data-stu-id="d4d7b-119">element\_description</span></span>

    <span data-ttu-id="d4d7b-120">Description du type d’élément de tableau.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-120">Description of the array element type.</span></span>

-   <span data-ttu-id="d4d7b-121">disposition du pointeur \_</span><span class="sxs-lookup"><span data-stu-id="d4d7b-121">pointer\_layout</span></span>

    <span data-ttu-id="d4d7b-122">Pour plus d’informations, consultez la rubrique [disposition du pointeur](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d7b-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="d4d7b-123">Tableaux de taille fixe</span><span class="sxs-lookup"><span data-stu-id="d4d7b-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="d4d7b-124">Une chaîne de format de tableau de taille fixe est générée pour les tableaux qui ont une taille connue et, par conséquent, peut être copiée par bloc dans la mémoire tampon de marshaling.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="d4d7b-125">Les deux formats de descripteur de tableau fixes sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="d4d7b-126">et</span><span class="sxs-lookup"><span data-stu-id="d4d7b-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="d4d7b-127">Tableau conforme</span><span class="sxs-lookup"><span data-stu-id="d4d7b-127">Conformant Array</span></span>

<span data-ttu-id="d4d7b-128">Un tableau conforme peut être copié par bloc une fois que la taille du tableau est connue.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="d4d7b-129">La description de la conformité \_<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="d4d7b-130">Tableau variable conforme</span><span class="sxs-lookup"><span data-stu-id="d4d7b-130">Conformant Varying Array</span></span>

<span data-ttu-id="d4d7b-131">Un tableau à variation conforme peut également être copié par bloc.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="d4d7b-132">La description de la conformité \_<> et la description de la variance \_<> est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="d4d7b-133">Tableau variable</span><span class="sxs-lookup"><span data-stu-id="d4d7b-133">Varying Array</span></span>

<span data-ttu-id="d4d7b-134">Les tableaux variables ont deux possibilités en fonction de la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="d4d7b-135">La description de l’écart \_<> est un descripteur de corrélation et a 4 ou 6 octets selon le [**/Robust**](/windows/desktop/Midl/-robust) utilisé.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="d4d7b-136">Pour les tableaux de variables incorporés à l’intérieur d’une structure, le champ décalage<2> de la description de l’écart \_<> est un décalage relatif de la position du tableau variable dans la structure à l’écart qui décrit le champ.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="d4d7b-137">Le décalage est généralement relatif au début de la structure.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="d4d7b-138">Tableaux complexes</span><span class="sxs-lookup"><span data-stu-id="d4d7b-138">Complex Arrays</span></span>

<span data-ttu-id="d4d7b-139">Un tableau complexe est un tableau avec un élément qui l’empêche d’être copié par bloc, et par conséquent, une action supplémentaire doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="d4d7b-140">Ces éléments rendent un tableau complexe :</span><span class="sxs-lookup"><span data-stu-id="d4d7b-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="d4d7b-141">types simples : ENUM16, \_ \_ INT3264 (sur les plateformes 64 bits uniquement), un intégral avec \[ [ **Range**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="d4d7b-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="d4d7b-142">pointeurs d’interface et de référence (tous les pointeurs sur les plateformes 64 bits)</span><span class="sxs-lookup"><span data-stu-id="d4d7b-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="d4d7b-143">unions</span><span class="sxs-lookup"><span data-stu-id="d4d7b-143">unions</span></span>
-   <span data-ttu-id="d4d7b-144">structures complexes (consultez la rubrique Description de la structure complexe pour obtenir une liste complète des raisons pour lesquelles une structure est complexe)</span><span class="sxs-lookup"><span data-stu-id="d4d7b-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="d4d7b-145">éléments définis avec \[ [**transmit \_ As**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ Marshal d’utilisateur**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="d4d7b-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="d4d7b-146">Tous les tableaux multidimensionnels avec au moins une dimension en conformité et/ou variable sont complexes, quel que soit le type d’élément sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="d4d7b-147">La description du tableau complexe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d4d7b-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="d4d7b-148">Le nombre \_ d' \_ éléments<2> champ est zéro si le tableau est conforme.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="d4d7b-149">La description de la conformité \_<> et la description de la variance \_<> est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="d4d7b-150">Si le tableau est conforme et/ou variance, la description de la conformité \_<> et/ou la description de la variance \_<> champ (s) ont des descriptions valides, sinon les 4 premiers octets du descripteur de corrélation sont définis sur 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="d4d7b-151">Les indicateurs, le cas échéant, sont définis sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d4d7b-151">The flags, when present, are set to zero.</span></span>

 

 
