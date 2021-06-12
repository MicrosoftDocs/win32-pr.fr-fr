---
title: vs_2_0
description: En savoir plus sur vs_2_0, un nuanceur de sommet programmable, qui est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010852"
---
# <a name="vs_2_0"></a><span data-ttu-id="604b1-103">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="604b1-103">vs\_2\_0</span></span>

<span data-ttu-id="604b1-104">Un nuanceur de sommet programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de vertex.</span><span class="sxs-lookup"><span data-stu-id="604b1-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="604b1-105">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="604b1-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="604b1-106">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="604b1-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="604b1-107">[Instructions-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contient une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="604b1-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="604b1-108">[Registres-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="604b1-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="604b1-109">Les [modificateurs de Registre du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers.md) permettent de modifier la façon dont une instruction fonctionne.</span><span class="sxs-lookup"><span data-stu-id="604b1-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="604b1-110">Les [modificateurs de Registre source du nuanceur de sommets](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="604b1-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="604b1-111">Le [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="604b1-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="604b1-112">Le [masquage du registre de destination](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="604b1-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="604b1-113">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="604b1-113">Instruction Count</span></span>

<span data-ttu-id="604b1-114">Chaque nuanceur de sommets peut avoir jusqu’à 256 instructions stockées.</span><span class="sxs-lookup"><span data-stu-id="604b1-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="604b1-115">Le nombre d’instructions exécutées peut être bien plus élevé (en raison de la prise en charge de la boucle/REP) et est limité par D3DCAPS9. MaxVShaderInstructionsExecuted, qui doit être au moins 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="604b1-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="604b1-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="604b1-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="604b1-117">Nuanceurs vertex</span><span class="sxs-lookup"><span data-stu-id="604b1-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




