---
title: vs_2_0
description: Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex. Enregistre les données de transfert dans et en dehors de l’ALU. Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971446"
---
# <a name="vs_2_0"></a><span data-ttu-id="80a7e-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80a7e-105">vs\_2\_0</span></span>

<span data-ttu-id="80a7e-106">Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="80a7e-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="80a7e-107">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="80a7e-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="80a7e-108">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="80a7e-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="80a7e-109">[Instructions-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contient une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="80a7e-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="80a7e-110">[Registres-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="80a7e-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="80a7e-111">Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="80a7e-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="80a7e-112">Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="80a7e-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="80a7e-113">Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="80a7e-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="80a7e-114">Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="80a7e-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="80a7e-115">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="80a7e-115">Instruction Count</span></span>

<span data-ttu-id="80a7e-116">Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées.</span><span class="sxs-lookup"><span data-stu-id="80a7e-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="80a7e-117">Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par D3DCAPS9. MaxVShaderInstructionsExecuted, qui doit être au moins 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="80a7e-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80a7e-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80a7e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80a7e-119">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="80a7e-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




