---
description: L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilisations et littéraux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513299"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="af649-103">Utilisations et littéraux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="af649-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="af649-104">L’utilisation est similaire à la portée d’un paramètre, car elle définit la portée dans laquelle le paramètre est valide.</span><span class="sxs-lookup"><span data-stu-id="af649-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af649-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="af649-105">Value</span></span>  | <span data-ttu-id="af649-106">Description</span><span class="sxs-lookup"><span data-stu-id="af649-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="af649-107">const</span><span class="sxs-lookup"><span data-stu-id="af649-107">const</span></span>  | <span data-ttu-id="af649-108">Le paramètre sera constant dans la portée de toutes les fonctions.</span><span class="sxs-lookup"><span data-stu-id="af649-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="af649-109">(Notez que ces paramètres peuvent toujours être écrits avec [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), car cela se produit en dehors de l’étendue de toutes les fonctions.)</span><span class="sxs-lookup"><span data-stu-id="af649-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="af649-110">partagés</span><span class="sxs-lookup"><span data-stu-id="af649-110">shared</span></span> | <span data-ttu-id="af649-111">Le paramètre sera partagé dans le pool d’effets.</span><span class="sxs-lookup"><span data-stu-id="af649-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="af649-112">static</span><span class="sxs-lookup"><span data-stu-id="af649-112">static</span></span> | <span data-ttu-id="af649-113">Le paramètre sera invisible pour l’application, autrement dit, vous ne pouvez pas y accéder à partir de [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="af649-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="af649-114">Le marquage d’un paramètre en tant que littéral indique que sa valeur ne changera jamais.</span><span class="sxs-lookup"><span data-stu-id="af649-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="af649-115">Cela permet au compilateur d’effet d’effectuer une optimisation supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="af649-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="af649-116">Seuls les paramètres de niveau supérieur non partagés peuvent être marqués comme Literal.</span><span class="sxs-lookup"><span data-stu-id="af649-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="af649-117">Les paramètres peuvent uniquement être marqués comme Literal avec [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="af649-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="af649-118">Les valeurs littérales ne peuvent pas être définies avec [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="af649-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af649-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af649-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af649-120">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="af649-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



