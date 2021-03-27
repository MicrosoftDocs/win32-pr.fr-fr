---
title: Registre d’entrée
description: Registre d’entrée
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940108"
---
# <a name="input-register"></a><span data-ttu-id="09583-103">Registre d’entrée</span><span class="sxs-lookup"><span data-stu-id="09583-103">Input Register</span></span>

<span data-ttu-id="09583-104">Registre d’entrée du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="09583-104">Vertex shader input register.</span></span>

<span data-ttu-id="09583-105">Les données de chaque vertex (à l’aide d’un ou plusieurs flux de vertex d’entrée) sont chargées dans les registres d’entrée de vertex avant l’exécution du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="09583-105">Data from each vertex (using one or more input vertex streams) is loaded into the vertex input registers before the vertex shader is run.</span></span> <span data-ttu-id="09583-106">Les registres d’entrée sont constitués de vecteurs à virgule flottante 16 4 composant, désignés comme v0 par v15.</span><span class="sxs-lookup"><span data-stu-id="09583-106">The input registers consist of 16 four-component floating-point vectors, designated as v0 through v15.</span></span> <span data-ttu-id="09583-107">Ces registres sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09583-107">These registers are read-only.</span></span> <span data-ttu-id="09583-108">Un registre d’entrée est lié aux données de vertex par le biais d’une déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="09583-108">An input register is bound to vertex data through a vertex declaration.</span></span>

<span data-ttu-id="09583-109">Les propriétés de Registre suivantes contrôlent le comportement de chaque registre :</span><span class="sxs-lookup"><span data-stu-id="09583-109">The following register properties control how each register behaves:</span></span>



| <span data-ttu-id="09583-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="09583-110">Property</span></span>        | <span data-ttu-id="09583-111">Description</span><span class="sxs-lookup"><span data-stu-id="09583-111">Description</span></span>                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="09583-112">Nom</span><span class="sxs-lookup"><span data-stu-id="09583-112">Name</span></span>            | <span data-ttu-id="09583-113">v \[ n \] -n est un numéro de Registre facultatif.</span><span class="sxs-lookup"><span data-stu-id="09583-113">v\[n\] - n is an optional register number.</span></span> <span data-ttu-id="09583-114">0 est la valeur par défaut utilisée, si elle est omise.</span><span class="sxs-lookup"><span data-stu-id="09583-114">0 is the default value used, if it is omitted.</span></span>     |
| <span data-ttu-id="09583-115">Count</span><span class="sxs-lookup"><span data-stu-id="09583-115">Count</span></span>           | <span data-ttu-id="09583-116">Un maximum de 16 registres, V0-v15.</span><span class="sxs-lookup"><span data-stu-id="09583-116">A maximum of 16 registers, v0 - v15.</span></span>                                                          |
| <span data-ttu-id="09583-117">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="09583-117">I/O permissions</span></span> | <span data-ttu-id="09583-118">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09583-118">Read-only.</span></span> <span data-ttu-id="09583-119">Ce registre ne peut pas être écrit par l’API ou dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="09583-119">This register cannot be written by the API or within the shader.</span></span>                   |
| <span data-ttu-id="09583-120">Ports de lecture</span><span class="sxs-lookup"><span data-stu-id="09583-120">Read ports</span></span>      | <span data-ttu-id="09583-121">1. il s’agit du nombre de fois qu’un registre peut être lu dans une instruction unique.</span><span class="sxs-lookup"><span data-stu-id="09583-121">1. This is the number of times a register can be read within a single instruction.</span></span> <span data-ttu-id="09583-122">Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="09583-122">See below.</span></span> |



 

<span data-ttu-id="09583-123">Toute instruction unique ne peut accéder qu’à un seul registre d’entrée de vertex.</span><span class="sxs-lookup"><span data-stu-id="09583-123">Any single instruction can access only one vertex input register.</span></span> <span data-ttu-id="09583-124">Toutefois, chaque source de l’instruction peut Swizzle et inverser ce vecteur au fur et à mesure de sa lecture.</span><span class="sxs-lookup"><span data-stu-id="09583-124">However, each source in the instruction can independently swizzle and negate that vector as it is read.</span></span>

## <a name="example"></a><span data-ttu-id="09583-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="09583-125">Example</span></span>

<span data-ttu-id="09583-126">Voici un exemple d’utilisation d’une déclaration de vertex pour lier des données de position de vertex 2D pour inscrire v0.</span><span class="sxs-lookup"><span data-stu-id="09583-126">Here is an example using a vertex declaration to bind 2D vertex position data to register v0.</span></span>

<span data-ttu-id="09583-127">La déclaration de vertex appartient à l’application :</span><span class="sxs-lookup"><span data-stu-id="09583-127">The vertex declaration belongs in the application:</span></span>


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



<span data-ttu-id="09583-128">Voici la déclaration du nuanceur de sommets correspondant :</span><span class="sxs-lookup"><span data-stu-id="09583-128">Here is the corresponding vertex shader declaration:</span></span>


```
dcl_position v0
```





| <span data-ttu-id="09583-129">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="09583-129">Vertex shader versions</span></span> | <span data-ttu-id="09583-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="09583-130">1\_1</span></span> | <span data-ttu-id="09583-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09583-131">2\_0</span></span> | <span data-ttu-id="09583-132">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="09583-132">2\_sw</span></span> | <span data-ttu-id="09583-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="09583-133">2\_x</span></span> | <span data-ttu-id="09583-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09583-134">3\_0</span></span> | <span data-ttu-id="09583-135">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="09583-135">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="09583-136">Registre de position</span><span class="sxs-lookup"><span data-stu-id="09583-136">Position Register</span></span>      | <span data-ttu-id="09583-137">x</span><span class="sxs-lookup"><span data-stu-id="09583-137">x</span></span>    | <span data-ttu-id="09583-138">x</span><span class="sxs-lookup"><span data-stu-id="09583-138">x</span></span>    | <span data-ttu-id="09583-139">x</span><span class="sxs-lookup"><span data-stu-id="09583-139">x</span></span>     | <span data-ttu-id="09583-140">x</span><span class="sxs-lookup"><span data-stu-id="09583-140">x</span></span>    | <span data-ttu-id="09583-141">x</span><span class="sxs-lookup"><span data-stu-id="09583-141">x</span></span>    | <span data-ttu-id="09583-142">x</span><span class="sxs-lookup"><span data-stu-id="09583-142">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="09583-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09583-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09583-144">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="09583-144">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




