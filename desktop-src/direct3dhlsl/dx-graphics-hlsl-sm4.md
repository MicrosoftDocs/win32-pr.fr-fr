---
title: Nuanceur modèle 4
description: Le nuancier modèle 4 est un sur-ensemble des fonctionnalités du nuanceur modèle 3, sauf que le nuanceur modèle 4 ne prend pas en charge les fonctionnalités du nuanceur modèle 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381417"
---
# <a name="shader-model-4"></a><span data-ttu-id="c09c6-103">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="c09c6-103">Shader Model 4</span></span>

<span data-ttu-id="c09c6-104">Le nuancier modèle 4 est un sur-ensemble des fonctionnalités du [nuanceur modèle 3](dx-graphics-hlsl-sm3.md), sauf que le nuanceur modèle 4 ne prend pas en charge les fonctionnalités du nuanceur modèle 1.</span><span class="sxs-lookup"><span data-stu-id="c09c6-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="c09c6-105">Il a été conçu à l’aide d’un noyau-nuanceur commun qui fournit un ensemble commun de fonctionnalités à tous les nuanceurs programmables, qui sont uniquement programmables à l’aide du langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="c09c6-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c09c6-106">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="c09c6-106">Feature</span></span></th>
<th><span data-ttu-id="c09c6-107">Utilité</span><span class="sxs-lookup"><span data-stu-id="c09c6-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c09c6-108">Jeu d'instructions</span><span class="sxs-lookup"><span data-stu-id="c09c6-108">Instruction Set</span></span></td>
<td><span data-ttu-id="c09c6-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="c09c6-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09c6-110">Ensemble de registres</span><span class="sxs-lookup"><span data-stu-id="c09c6-110">Register Set</span></span></td>
<td><span data-ttu-id="c09c6-111">Le jeu de registres est accessible via des membres dans des mémoires tampons de constante et de texture à l’aide de la sémantique HLSL pour des éléments tels que la compression de composants.</span><span class="sxs-lookup"><span data-stu-id="c09c6-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="c09c6-112">Registres de nuanceur de pixels (voir <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers-ps_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registers-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="c09c6-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="c09c6-113">Registres de nuanceur vertex (voir <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers-vs_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registers-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="c09c6-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="c09c6-114">Registres de nuanceur Geometry (voir <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registres-gs_4_0</a> et <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registres-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="c09c6-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09c6-115">Vertex shader Max</span><span class="sxs-lookup"><span data-stu-id="c09c6-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="c09c6-116">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="c09c6-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09c6-117">Nuanceur de pixels max.</span><span class="sxs-lookup"><span data-stu-id="c09c6-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="c09c6-118">Pas de restriction</span><span class="sxs-lookup"><span data-stu-id="c09c6-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c09c6-119">Nouveaux profils de nuanceur ajoutés</span><span class="sxs-lookup"><span data-stu-id="c09c6-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="c09c6-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="c09c6-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c09c6-121">Nouveau profil de Effect-Framework ajouté</span><span class="sxs-lookup"><span data-stu-id="c09c6-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="c09c6-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="c09c6-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c09c6-123">\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 et FX \_ 4 \_ 1 sont pris en charge sur Direct3D 10,1 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c09c6-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="c09c6-124">Le Shader Model 4 prend en charge une nouvelle étape de pipeline, l’étape Geometry-Shader, qui peut être utilisée pour créer ou modifier une géométrie existante.</span><span class="sxs-lookup"><span data-stu-id="c09c6-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="c09c6-125">Il comprend également deux nouveaux types d’objets : un objet de sortie de flux conçu pour la diffusion en continu de données à partir de l’étape Geometry, et un objet texture basé sur un modèle qui implémente les fonctions d’échantillonnage de texture.</span><span class="sxs-lookup"><span data-stu-id="c09c6-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="c09c6-126">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="c09c6-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="c09c6-127">Constantes</span><span class="sxs-lookup"><span data-stu-id="c09c6-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="c09c6-128">Geometry-objet Shader</span><span class="sxs-lookup"><span data-stu-id="c09c6-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="c09c6-129">Stream-sortie (objet)</span><span class="sxs-lookup"><span data-stu-id="c09c6-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="c09c6-130">Texture, objet</span><span class="sxs-lookup"><span data-stu-id="c09c6-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="c09c6-131">Le modèle de nuanceur 4 prend en charge les règles de compression qui déterminent la façon dont les données peuvent être réorganisées lors de leur stockage.</span><span class="sxs-lookup"><span data-stu-id="c09c6-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="c09c6-132">Ces règles sont décrites dans [règles de compression pour les variables constantes](dx-graphics-hlsl-packing-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="c09c6-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="c09c6-133">La section [Shader Model 4 assembly](dx-graphics-hlsl-sm4-asm.md) décrit les instructions d’assembly que les nuanciers Model 4 et shader model 4,1 prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="c09c6-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c09c6-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c09c6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c09c6-135">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="c09c6-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




