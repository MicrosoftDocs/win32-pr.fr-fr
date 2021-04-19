---
description: Options d’habillage de texture pour les API de calcul IMT.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: D3DXIMT FLAGs, énumération (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539877"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="dac6f-103">Énumération d’indicateurs D3DXIMT</span><span class="sxs-lookup"><span data-stu-id="dac6f-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="dac6f-104">Options d’habillage de texture pour les API de calcul IMT.</span><span class="sxs-lookup"><span data-stu-id="dac6f-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dac6f-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="dac6f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dac6f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dac6f-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="dac6f-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="dac6f-108">La texture est renvoyée à la ligne dans la direction U.</span><span class="sxs-lookup"><span data-stu-id="dac6f-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="dac6f-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="dac6f-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="dac6f-110">La texture est renvoyée à la ligne dans la direction V.</span><span class="sxs-lookup"><span data-stu-id="dac6f-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="dac6f-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ enveloppe \_ UV**</span><span class="sxs-lookup"><span data-stu-id="dac6f-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="dac6f-112">La texture est renvoyée à la ligne dans la direction V et V.</span><span class="sxs-lookup"><span data-stu-id="dac6f-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dac6f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dac6f-113">Requirements</span></span>



| <span data-ttu-id="dac6f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dac6f-114">Requirement</span></span> | <span data-ttu-id="dac6f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dac6f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dac6f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dac6f-116">Header</span></span><br/> | <dl> <span data-ttu-id="dac6f-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac6f-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac6f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dac6f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac6f-119">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="dac6f-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="dac6f-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="dac6f-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="dac6f-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="dac6f-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="dac6f-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="dac6f-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="dac6f-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="dac6f-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




