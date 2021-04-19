---
description: Jeton de version qui crée un remplissage de texture procédurale dans Effects. Cette macro est utilisée par les fonctions D3DXFillxxxTX.
ms.assetid: b11b6229-27a3-4813-9642-9e33bcd0da7a
title: D3DXTX_VERSION (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTX_VERSION
api_type:
- HeaderDef
api_location:
- D3DX9Shader.h
ms.openlocfilehash: 05b034a48635e3a5a6d1a3dbdfbabd0fe2933b5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522351"
---
# <a name="d3dxtx_version"></a><span data-ttu-id="44c57-104">VERSION de D3DXTX \_</span><span class="sxs-lookup"><span data-stu-id="44c57-104">D3DXTX\_VERSION</span></span>

<span data-ttu-id="44c57-105">Jeton de version qui crée un remplissage de texture procédurale dans Effects.</span><span class="sxs-lookup"><span data-stu-id="44c57-105">Version token that creates a procedural texture filler in effects.</span></span> <span data-ttu-id="44c57-106">Cette macro est utilisée par les fonctions D3DXFillxxxTX.</span><span class="sxs-lookup"><span data-stu-id="44c57-106">This macro is used by the D3DXFillxxxTX functions.</span></span>

``` syntax
#define D3DXTX_VERSION (_Major, _Minor) (('T' << 24) | ('X' << 16) | ((_Major) << 8) | (_Minor))
```

## <a name="return-value"></a><span data-ttu-id="44c57-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="44c57-107">Return Value</span></span>

<span data-ttu-id="44c57-108">La macro retourne le jeton de version de la texture procédurale.</span><span class="sxs-lookup"><span data-stu-id="44c57-108">The macro returns the procedural texture version token.</span></span>

## <a name="requirements"></a><span data-ttu-id="44c57-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44c57-109">Requirements</span></span>



| <span data-ttu-id="44c57-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44c57-110">Requirement</span></span> | <span data-ttu-id="44c57-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="44c57-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c57-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="44c57-112">Header</span></span><br/> | <dl> <span data-ttu-id="44c57-113"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="44c57-113"><dt>D3DX9Shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c57-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c57-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c57-115">Macros</span><span class="sxs-lookup"><span data-stu-id="44c57-115">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="44c57-116">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="44c57-116">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="44c57-117">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="44c57-117">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="44c57-118">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="44c57-118">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 




