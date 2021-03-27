---
title: Registre de coordonnées de texture (référence PS HLSL)
description: Registre d’entrée de nuanceur de pixels contenant des coordonnées de texture.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104971627"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="95442-103">Registre de coordonnées de texture (référence PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="95442-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="95442-104">Registre d’entrée de nuanceur de pixels contenant des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="95442-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="95442-105">Versions de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="95442-105">Pixel shader versions</span></span>       | <span data-ttu-id="95442-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="95442-106">1\_1</span></span> | <span data-ttu-id="95442-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="95442-107">1\_2</span></span> | <span data-ttu-id="95442-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="95442-108">1\_3</span></span> | <span data-ttu-id="95442-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="95442-109">1\_4</span></span> | <span data-ttu-id="95442-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95442-110">2\_0</span></span> | <span data-ttu-id="95442-111">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="95442-111">2\_sw</span></span> | <span data-ttu-id="95442-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="95442-112">2\_x</span></span> | <span data-ttu-id="95442-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="95442-113">3\_0</span></span> | <span data-ttu-id="95442-114">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="95442-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="95442-115">Registre de coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="95442-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="95442-116">x</span><span class="sxs-lookup"><span data-stu-id="95442-116">x</span></span>    | <span data-ttu-id="95442-117">x</span><span class="sxs-lookup"><span data-stu-id="95442-117">x</span></span>     | <span data-ttu-id="95442-118">x</span><span class="sxs-lookup"><span data-stu-id="95442-118">x</span></span>    | <span data-ttu-id="95442-119">x</span><span class="sxs-lookup"><span data-stu-id="95442-119">x</span></span>    | <span data-ttu-id="95442-120">x</span><span class="sxs-lookup"><span data-stu-id="95442-120">x</span></span>     |



 

<span data-ttu-id="95442-121">Un registre de coordonnées de texture contient des données de coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="95442-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="95442-122">Avant d’utiliser un registre de coordonnées de texture, il doit être déclaré par une déclaration de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="95442-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="95442-123">Pour plus d’informations sur la façon de déclarer un registre de texture, consultez [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="95442-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="95442-124">En outre, Voici d’autres propriétés des registres de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="95442-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="95442-125">Il y a huit registres de coordonnées de texture de nuanceur de pixels, T0 à T7.</span><span class="sxs-lookup"><span data-stu-id="95442-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="95442-126">Il s’agit de registres en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="95442-126">These are read-only registers.</span></span>
-   <span data-ttu-id="95442-127">Elles contiennent des valeurs RVBA à quatre composants à partir des vertex d’entrée.</span><span class="sxs-lookup"><span data-stu-id="95442-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="95442-128">Elles contiennent des valeurs de données de plage dynamique haute précision interpolées à partir des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="95442-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="95442-129">Les valeurs sont générées avec l’interpolation de perspective correcte.</span><span class="sxs-lookup"><span data-stu-id="95442-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="95442-130">Les données sont de précision à virgule flottante et sont signées.</span><span class="sxs-lookup"><span data-stu-id="95442-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="95442-131">Il n’y a qu’un maximum dans une seule instruction.</span><span class="sxs-lookup"><span data-stu-id="95442-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="95442-132">Plusieurs lectures d’un registre de coordonnées de texture dans un nuanceur doivent utiliser un [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)identique.</span><span class="sxs-lookup"><span data-stu-id="95442-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="95442-133">Le modificateur de précision partielle facultatif \[ \_ pp \] s’applique aux lectures dépendantes.</span><span class="sxs-lookup"><span data-stu-id="95442-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="95442-134">Cela est dû au fait que la précision partielle affecte les opérations arithmétiques impliquant le registre de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="95442-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="95442-135">Il n’affecte pas la précision des instructions d’adresse de texture, car il n’affecte pas les itérateurs de coordonnée de texture.</span><span class="sxs-lookup"><span data-stu-id="95442-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95442-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95442-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95442-137">Inscrit</span><span class="sxs-lookup"><span data-stu-id="95442-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




