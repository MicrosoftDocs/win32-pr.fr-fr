---
title: 'Texture2D :: Texture2D GatherCmp, méthodes'
description: Échantillonne et compare un Texture2D et retourne tous les composants.
ms.assetid: d520b113-77af-486e-8d3d-8276f72df18f
keywords:
- Méthodes GatherCmp HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 18455f33ba97c9d5a0180a59e39891cd617a09af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973899"
---
# <a name="texture2dgathercmp-methods"></a><span data-ttu-id="4bce9-104">Texture2D :: GatherCmp, méthodes</span><span class="sxs-lookup"><span data-stu-id="4bce9-104">Texture2D::GatherCmp methods</span></span>

<span data-ttu-id="4bce9-105">Pour quatre valeurs de Texel d’un [**Texture2D**](sm5-object-texture2d.md) qui seraient utilisées dans une opération de filtrage bilinéaire, retourne leur comparaison par rapport à une valeur de comparaison.</span><span class="sxs-lookup"><span data-stu-id="4bce9-105">For four texel values of a [**Texture2D**](sm5-object-texture2d.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="4bce9-106">Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4_c](./gather4-c--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="4bce9-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4bce9-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="4bce9-107">Overload list</span></span>



| <span data-ttu-id="4bce9-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="4bce9-108">Method</span></span>                                                                             | <span data-ttu-id="4bce9-109">Description</span><span class="sxs-lookup"><span data-stu-id="4bce9-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4bce9-110">**GatherCmp (S, float, float, int)**</span><span class="sxs-lookup"><span data-stu-id="4bce9-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2d-gathercmp.md)             | <span data-ttu-id="4bce9-111">Échantillonne et compare une texture et retourne les quatre composants.</span><span class="sxs-lookup"><span data-stu-id="4bce9-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="4bce9-112">**GatherCmp (S, float, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="4bce9-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="4bce9-113">Échantillonne et compare une texture et retourne les quatre composants, ainsi que l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="4bce9-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bce9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bce9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bce9-115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="4bce9-115">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> </dl>

 

