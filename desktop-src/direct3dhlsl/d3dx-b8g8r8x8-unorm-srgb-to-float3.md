---
title: D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3. | D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction)
ms.assetid: 9b3c511c-95c2-454c-95b9-ff6ab0920466
keywords:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277f10bc574e03a7bd608a333cba65f95a3e0b43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992137"
---
# <a name="d3dx_b8g8r8x8_unorm_srgb_to_float3-function"></a><span data-ttu-id="a137b-105">\_B8G8R8X8 \_ de D3DX UNORM \_ sRVB à la \_ \_ fonction FLOAT3</span><span class="sxs-lookup"><span data-stu-id="a137b-105">D3DX\_B8G8R8X8\_UNORM\_SRGB\_to\_FLOAT3 function</span></span>

<span data-ttu-id="a137b-106">Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT3.</span><span class="sxs-lookup"><span data-stu-id="a137b-106">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT3.</span></span>

## <a name="syntax"></a><span data-ttu-id="a137b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a137b-107">Syntax</span></span>

``` syntax
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="a137b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a137b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a137b-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="a137b-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a137b-110">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="a137b-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a137b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a137b-111">Return value</span></span>

<span data-ttu-id="a137b-112">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="a137b-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="a137b-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a137b-113">Requirements</span></span>



| <span data-ttu-id="a137b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a137b-114">Requirement</span></span> | <span data-ttu-id="a137b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a137b-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a137b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a137b-116">Header</span></span><br/> | <dl> <span data-ttu-id="a137b-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="a137b-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a137b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a137b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a137b-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="a137b-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="a137b-120">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="a137b-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





