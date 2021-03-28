---
title: 'TextureCube :: TextureCube, méthodes de regroupement'
description: 'Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire. | TextureCube :: TextureCube, méthodes de regroupement'
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
keywords:
- Méthodes de collecte HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974098"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="b2bd9-105">TextureCube :: Gather, méthodes</span><span class="sxs-lookup"><span data-stu-id="b2bd9-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="b2bd9-106">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="b2bd9-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="b2bd9-107">Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="b2bd9-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b2bd9-108">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="b2bd9-108">Overload list</span></span>



| <span data-ttu-id="b2bd9-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="b2bd9-109">Method</span></span>                                                     | <span data-ttu-id="b2bd9-110">Description</span><span class="sxs-lookup"><span data-stu-id="b2bd9-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2bd9-111">**Regroupement (S, float)**</span><span class="sxs-lookup"><span data-stu-id="b2bd9-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="b2bd9-112">Échantillonne une texture et retourne les quatre échantillons (composant rouge uniquement) qui sont utilisés pour l’interpolation bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="b2bd9-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="b2bd9-113">**Gather (S, float, uint)**</span><span class="sxs-lookup"><span data-stu-id="b2bd9-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="b2bd9-114">Échantillonne une texture et retourne les quatre composants, ainsi que l’état de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b2bd9-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="b2bd9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2bd9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bd9-116">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="b2bd9-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

