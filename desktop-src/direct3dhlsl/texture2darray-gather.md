---
title: 'Texture2DArray :: Texture2DArray, méthodes de regroupement'
description: Échantillonne un Texture2DArray et retourne les quatre composants.
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
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
ms.openlocfilehash: cd10959490a85583cab01814f9cdb012859317a4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973883"
---
# <a name="texture2darraygather-methods"></a><span data-ttu-id="4b5b0-104">Texture2DArray :: Gather, méthodes</span><span class="sxs-lookup"><span data-stu-id="4b5b0-104">Texture2DArray::Gather methods</span></span>

<span data-ttu-id="4b5b0-105">Retourne les quatre valeurs de Texel d’un [**Texture2DArray**](sm5-object-texture2darray.md) qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="4b5b0-105">Returns the four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="4b5b0-106">Pour plus d’informations sur la description de l’instruction DXBC sous-jacente, consultez la documentation sur [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="4b5b0-106">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4b5b0-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="4b5b0-107">Overload list</span></span>



| <span data-ttu-id="4b5b0-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="4b5b0-108">Method</span></span>                                                                | <span data-ttu-id="4b5b0-109">Description</span><span class="sxs-lookup"><span data-stu-id="4b5b0-109">Description</span></span>                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b5b0-110">**Gather (S, float, int)**</span><span class="sxs-lookup"><span data-stu-id="4b5b0-110">**Gather(S,float,int)**</span></span>](sm5-object-texture2darray-gather.md)        | <span data-ttu-id="4b5b0-111">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire.</span><span class="sxs-lookup"><span data-stu-id="4b5b0-111">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                 |
| [<span data-ttu-id="4b5b0-112">**Gather (S, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="4b5b0-112">**Gather(S,float,int,uint)**</span></span>](t2darray-gather-s-float-int-uint-.md)  | <span data-ttu-id="4b5b0-113">Retourne les quatre valeurs de Texel qui seraient utilisées dans une opération de filtrage bilinéaire, ainsi que l’état du mappage de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="4b5b0-113">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b5b0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b5b0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5b0-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4b5b0-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

