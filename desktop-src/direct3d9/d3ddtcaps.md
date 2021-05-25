---
description: Constantes décrivant les types de données de vertex pris en charge par un appareil.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343233"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="a3bba-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="a3bba-103">D3DDTCAPS</span></span>

<span data-ttu-id="a3bba-104">Constantes décrivant les types de données de vertex pris en charge par un appareil.</span><span class="sxs-lookup"><span data-stu-id="a3bba-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="a3bba-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="a3bba-105">\#define</span></span>              | <span data-ttu-id="a3bba-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3bba-106">Value</span></span>       | <span data-ttu-id="a3bba-107">Description</span><span class="sxs-lookup"><span data-stu-id="a3bba-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3bba-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="a3bba-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="a3bba-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="a3bba-109">0x00000001L</span></span> | <span data-ttu-id="a3bba-110">octet non signé 4D.</span><span class="sxs-lookup"><span data-stu-id="a3bba-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="a3bba-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="a3bba-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="a3bba-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="a3bba-112">0x00000002L</span></span> | <span data-ttu-id="a3bba-113">Octets non signés normalisés et 4D.</span><span class="sxs-lookup"><span data-stu-id="a3bba-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="a3bba-114">Chacun des quatre octets est normalisé en divisant à 255,0.</span><span class="sxs-lookup"><span data-stu-id="a3bba-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="a3bba-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="a3bba-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="a3bba-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="a3bba-116">0x00000004L</span></span> | <span data-ttu-id="a3bba-117">Normald, unsigned short, Expanded to (First Byte/32767.0, second Byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a3bba-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="a3bba-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="a3bba-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="a3bba-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="a3bba-119">0x00000008L</span></span> | <span data-ttu-id="a3bba-120">Normalized, 4D signé Short, développé sur (First Byte/32767.0, second Byte/32767.0, Third Byte/32767.0, quatrième octet/32767.0).</span><span class="sxs-lookup"><span data-stu-id="a3bba-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="a3bba-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="a3bba-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="a3bba-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="a3bba-122">0x00000010L</span></span> | <span data-ttu-id="a3bba-123">Normalized, 2J unsigned short, Expanded to (First Byte/65535.0, second Byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="a3bba-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="a3bba-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="a3bba-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="a3bba-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a3bba-125">0x00000020L</span></span> | <span data-ttu-id="a3bba-126">4D normalisé non signé, développé sur (premier octet/65535.0, deuxième octet/65535.0, troisième octet/65535.0, quatrième octet/65535.0).</span><span class="sxs-lookup"><span data-stu-id="a3bba-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="a3bba-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="a3bba-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="a3bba-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="a3bba-128">0x00000040L</span></span> | <span data-ttu-id="a3bba-129">format 3D non signé 10 10 10 développé sur (valeur, valeur, valeur, 1).</span><span class="sxs-lookup"><span data-stu-id="a3bba-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="a3bba-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="a3bba-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="a3bba-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="a3bba-131">0x00000080L</span></span> | <span data-ttu-id="a3bba-132">format 3D signé 10 10 10 normalisé et développé en (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="a3bba-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="a3bba-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a3bba-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="a3bba-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a3bba-134">0x00000100L</span></span> | <span data-ttu-id="a3bba-135">nombres à virgule flottante 2D 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a3bba-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="a3bba-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="a3bba-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="a3bba-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="a3bba-137">0x00000200L</span></span> | <span data-ttu-id="a3bba-138">nombres à virgule flottante 4D 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a3bba-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="a3bba-139">Ces constantes sont utilisées par le membre DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a3bba-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a3bba-140">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="a3bba-140">Constant Information</span></span>



|  <span data-ttu-id="a3bba-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3bba-141">Requirement</span></span>                        | <span data-ttu-id="a3bba-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3bba-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="a3bba-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3bba-143">Header</span></span>                   | <span data-ttu-id="a3bba-144">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a3bba-144">d3d9caps.h</span></span> |
| <span data-ttu-id="a3bba-145">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="a3bba-145">Minimum operating system</span></span> | <span data-ttu-id="a3bba-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a3bba-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a3bba-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3bba-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3bba-148">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="a3bba-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



