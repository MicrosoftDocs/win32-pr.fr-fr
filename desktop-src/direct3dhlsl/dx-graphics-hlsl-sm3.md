---
title: Modèle de nuanceur 3
description: Le modèle de nuanceur 3 a ajouté des fonctionnalités supplémentaires au nuanceur modèle 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383048"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="053a2-103">Shader Model 3 (référence HLSL)</span><span class="sxs-lookup"><span data-stu-id="053a2-103">Shader Model 3 (HLSL reference)</span></span>

<span data-ttu-id="053a2-104">Le modèle de nuanceur 3 a ajouté des fonctionnalités supplémentaires au [nuanceur modèle 2](dx-graphics-hlsl-sm2.md).</span><span class="sxs-lookup"><span data-stu-id="053a2-104">Shader Model 3 added additional capabilities to [shader model 2](dx-graphics-hlsl-sm2.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="053a2-105">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="053a2-105">Feature</span></span></td>
<td><span data-ttu-id="053a2-106">Utilité</span><span class="sxs-lookup"><span data-stu-id="053a2-106">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="053a2-107">Jeu d'instructions</span><span class="sxs-lookup"><span data-stu-id="053a2-107">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="053a2-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="053a2-108"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="053a2-109">Instructions d’assembly (voir instructions <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instructions-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="053a2-109">Assembly instructions (see <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0 Instructions</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">Instructions - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="053a2-110">Ensemble de registres</span><span class="sxs-lookup"><span data-stu-id="053a2-110">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="053a2-111">Registres de nuanceur de pixels (voir <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">registres ps_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="053a2-111">Pixel shader registers (see <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">ps_3_0 Registers</a>)</span></span></li>
<li><span data-ttu-id="053a2-112">Registres de nuanceur vertex (voir <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers-vs_3_0</a>)</span><span class="sxs-lookup"><span data-stu-id="053a2-112">Vertex shader registers (see <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers - vs_3_0</a>)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="053a2-113">Nuanceur de pixels max.</span><span class="sxs-lookup"><span data-stu-id="053a2-113">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="053a2-114">512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxPixelShader30InstructionSlots (voir <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="053a2-114">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="053a2-115">Vertex shader Max</span><span class="sxs-lookup"><span data-stu-id="053a2-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="053a2-116">512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxVertexShader30InstructionSlots (voir <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="053a2-116">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots (see <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="053a2-117">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="053a2-117">Shader Profiles</span></span></td>
<td><span data-ttu-id="053a2-118">ps_3_0, vs_3_0</span><span class="sxs-lookup"><span data-stu-id="053a2-118">ps_3_0, vs_3_0</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="053a2-119">Pour plus d’informations sur les nuanceurs de modèle 3, consultez :</span><span class="sxs-lookup"><span data-stu-id="053a2-119">For more details on model 3 shaders, see:</span></span>

-   [<span data-ttu-id="053a2-120">Nuanceur de pixels 3,0</span><span class="sxs-lookup"><span data-stu-id="053a2-120">Pixel Shader 3.0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)
-   [<span data-ttu-id="053a2-121">Vertex Shader 3,0</span><span class="sxs-lookup"><span data-stu-id="053a2-121">Vertex Shader 3.0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a><span data-ttu-id="053a2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="053a2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="053a2-123">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="053a2-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 