---
title: D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8A8 UNORM dans un XMFLOAT4. | D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction)
ms.assetid: f6ce6125-c67e-4545-b25e-3400c0fc62b1
keywords:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91311bb83aa034410361bea631aa79f86737ff65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322697"
---
# <a name="d3dx_b8g8r8a8_unorm_srgb_to_float4-function"></a><span data-ttu-id="51c91-105">\_B8G8R8A8 \_ de D3DX UNORM \_ sRVB à la \_ \_ fonction float4</span><span class="sxs-lookup"><span data-stu-id="51c91-105">D3DX\_B8G8R8A8\_UNORM\_SRGB\_to\_FLOAT4 function</span></span>

<span data-ttu-id="51c91-106">Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8A8 UNORM dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="51c91-106">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c91-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51c91-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="51c91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51c91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c91-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="51c91-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="51c91-110">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="51c91-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c91-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51c91-111">Return value</span></span>

<span data-ttu-id="51c91-112">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="51c91-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="51c91-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="51c91-113">Requirements</span></span>



| <span data-ttu-id="51c91-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51c91-114">Requirement</span></span> | <span data-ttu-id="51c91-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="51c91-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51c91-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="51c91-116">Header</span></span><br/> | <dl> <span data-ttu-id="51c91-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="51c91-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c91-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c91-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c91-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="51c91-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="51c91-120">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="51c91-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





