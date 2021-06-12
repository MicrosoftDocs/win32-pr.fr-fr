---
title: ps_2_0
description: En savoir plus sur ps_2_0, un nuanceur de pixels programmable, qui est constitué d’un ensemble d’instructions qui s’appliquent aux données de pixels.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010982"
---
# <a name="ps_2_0"></a><span data-ttu-id="85196-103">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="85196-103">ps\_2\_0</span></span>

<span data-ttu-id="85196-104">Un nuanceur de pixels programmable est constitué d’un ensemble d’instructions qui fonctionnent sur des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="85196-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="85196-105">Enregistre les données de transfert dans et en dehors de l’ALU.</span><span class="sxs-lookup"><span data-stu-id="85196-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="85196-106">Un contrôle supplémentaire peut être appliqué pour modifier l’instruction, les résultats ou les données qui sont écrites.</span><span class="sxs-lookup"><span data-stu-id="85196-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="85196-107">[les \_ instructions PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contiennent une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="85196-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="85196-108">[ \_ registres PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) répertorie les différents types de registres utilisés par le nuanceur de sommets alu.</span><span class="sxs-lookup"><span data-stu-id="85196-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="85196-109">[Modificateurs](dx9-graphics-reference-asm-ps-registers-modifiers.md) Sont utilisées pour modifier le mode de fonctionnement d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="85196-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="85196-110">Le [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) détermine les composants du registre de destination qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="85196-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="85196-111">Les [modificateurs de Registre source du nuanceur de pixels](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) modifient les données du Registre source avant l’exécution de l’instruction.</span><span class="sxs-lookup"><span data-stu-id="85196-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="85196-112">Le [Registre source Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) offre un contrôle supplémentaire sur les composants Register qui sont lus, copiés ou écrits.</span><span class="sxs-lookup"><span data-stu-id="85196-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="85196-113">Nombre d’instructions</span><span class="sxs-lookup"><span data-stu-id="85196-113">Instruction Count</span></span>

<span data-ttu-id="85196-114">Les nuanceurs présentent des restrictions pour le nombre maximal d’instructions.</span><span class="sxs-lookup"><span data-stu-id="85196-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="85196-115">Nombre total d’emplacements d’instructions : 96 (64 arithmétique et 32 texture).</span><span class="sxs-lookup"><span data-stu-id="85196-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="85196-116">Nombre d’échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="85196-116">Sampler Count</span></span>

<span data-ttu-id="85196-117">Le nombre d’échantillonneurs de texture disponibles est 16.</span><span class="sxs-lookup"><span data-stu-id="85196-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85196-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85196-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85196-119">Nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="85196-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




