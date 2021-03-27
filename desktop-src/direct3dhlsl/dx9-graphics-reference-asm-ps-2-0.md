---
title: ps_2_0
description: Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971326"
---
# <a name="ps_2_0"></a><span data-ttu-id="70ea8-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="70ea8-105">ps\_2\_0</span></span>

<span data-ttu-id="70ea8-106">Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="70ea8-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="70ea8-107">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="70ea8-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="70ea8-108">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="70ea8-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="70ea8-109">[les \_ instructions PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contiennent une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="70ea8-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="70ea8-110">[ \_ registres PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="70ea8-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="70ea8-111">[Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="70ea8-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="70ea8-112">Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="70ea8-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="70ea8-113">Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="70ea8-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="70ea8-114">Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="70ea8-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="70ea8-115">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="70ea8-115">Instruction Count</span></span>

<span data-ttu-id="70ea8-116">Les nuanceurs présentent des restrictions pour le nombre maximal d’instructions.</span><span class="sxs-lookup"><span data-stu-id="70ea8-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="70ea8-117">Nombre total d’emplacements d’instructions : 96 (64 arithmétique et 32 texture).</span><span class="sxs-lookup"><span data-stu-id="70ea8-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="70ea8-118">Nombre d’échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="70ea8-118">Sampler Count</span></span>

<span data-ttu-id="70ea8-119">Le nombre d’échantillonneurs de texture disponibles est 16.</span><span class="sxs-lookup"><span data-stu-id="70ea8-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70ea8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70ea8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70ea8-121">Nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="70ea8-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




