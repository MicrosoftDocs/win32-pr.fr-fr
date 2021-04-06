---
title: Modèle de nuanceur 1
description: Le modèle de nuanceur 1 était le premier modèle de nuanceur créé dans DirectX. Il a introduit les nuanceurs vertex et pixel dans la première implémentation du pipeline programmable.
ms.assetid: 565ee7b5-1266-4e2f-8c22-c0e60b8c4619
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ebbc28c1c10ef112bf7be3b500be7f4ecaa6481
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104032009"
---
# <a name="shader-model-1"></a><span data-ttu-id="bec87-104">Modèle de nuanceur 1</span><span class="sxs-lookup"><span data-stu-id="bec87-104">Shader Model 1</span></span>

<span data-ttu-id="bec87-105">Le modèle de nuanceur 1 était le premier modèle de nuanceur créé dans DirectX.</span><span class="sxs-lookup"><span data-stu-id="bec87-105">Shader Model 1 was the first shader model created in DirectX.</span></span> <span data-ttu-id="bec87-106">Il a introduit les nuanceurs vertex et pixel dans la première implémentation du pipeline programmable.</span><span class="sxs-lookup"><span data-stu-id="bec87-106">It introduced vertex and pixel shaders to the first implementation of the programmable pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bec87-107">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="bec87-107">Feature</span></span></td>
<td><span data-ttu-id="bec87-108">Utilité</span><span class="sxs-lookup"><span data-stu-id="bec87-108">Capability</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bec87-109">Jeu d'instructions</span><span class="sxs-lookup"><span data-stu-id="bec87-109">Instruction Set</span></span></td>
<td><ul>
<li><span data-ttu-id="bec87-110"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="bec87-110"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></li>
<li><span data-ttu-id="bec87-111">Instructions de l’assembly du nuanceur de sommets (voir <a href="dx9-graphics-reference-asm-vs-instructions-vs-1-1.md">instructions-vs_1_1</a>).</span><span class="sxs-lookup"><span data-stu-id="bec87-111">Vertex shader assembly instructions (see <a href="dx9-graphics-reference-asm-vs-instructions-vs-1-1.md">Instructions - vs_1_1</a>).</span></span> <span data-ttu-id="bec87-112">La prise en charge des instructions de nuanceur de pixels (ps_1_x) est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="bec87-112">Support for pixel shader instructions (ps_1_x) has been deprecated.</span></span> <span data-ttu-id="bec87-113">Pour compiler ps_1_x nuanceurs comme des nuanceurs de ps_2_0, consultez <a href="/windows/desktop/direct3dtools/dx-graphics-tools-fxc-using">compilation du modèle de nuanceur 1</a>.</span><span class="sxs-lookup"><span data-stu-id="bec87-113">To compile ps_1_x shaders as ps_2_0 shaders see <a href="/windows/desktop/direct3dtools/dx-graphics-tools-fxc-using">Compiling Shader Model 1</a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bec87-114">Ensemble de registres</span><span class="sxs-lookup"><span data-stu-id="bec87-114">Register Set</span></span></td>
<td><ul>
<li><span data-ttu-id="bec87-115"><a href="dx9-graphics-reference-asm-vs-registers-vs-1-1.md">Registres de nuanceur vertex</a></span><span class="sxs-lookup"><span data-stu-id="bec87-115"><a href="dx9-graphics-reference-asm-vs-registers-vs-1-1.md">Vertex shader registers</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bec87-116">Vertex shader Max</span><span class="sxs-lookup"><span data-stu-id="bec87-116">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="bec87-117">instructions 128</span><span class="sxs-lookup"><span data-stu-id="bec87-117">128 instructions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bec87-118">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="bec87-118">Shader Profiles</span></span></td>
<td><span data-ttu-id="bec87-119">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="bec87-119">vs_1_1</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bec87-120">Pour plus d’informations sur le Shader Model 1, consultez :</span><span class="sxs-lookup"><span data-stu-id="bec87-120">For more details on shader model 1, see:</span></span>

-   [<span data-ttu-id="bec87-121">Nuanceur de sommets</span><span class="sxs-lookup"><span data-stu-id="bec87-121">Vertex Shader</span></span>](dx9-graphics-reference-asm-vs-1-1.md)

## <a name="related-topics"></a><span data-ttu-id="bec87-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bec87-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bec87-123">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="bec87-123">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 