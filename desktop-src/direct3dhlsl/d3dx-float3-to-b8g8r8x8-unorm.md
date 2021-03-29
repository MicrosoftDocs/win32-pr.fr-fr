---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM fonction)
description: Compresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM uint.
ms.assetid: 9492578b-e3c3-4856-b6d2-49f776a21d77
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d922264c62526b79aec5d3e36bb477e6a62987
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992208"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm-function"></a><span data-ttu-id="18f9e-104">D3DX \_ FLOAT3 \_ vers \_ B8G8R8X8 \_ UNORM, fonction</span><span class="sxs-lookup"><span data-stu-id="18f9e-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM function</span></span>

<span data-ttu-id="18f9e-105">Compresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM uint.</span><span class="sxs-lookup"><span data-stu-id="18f9e-105">Packs the given XMFLOAT3 into a DXGI\_FORMAT\_B8G8R8X8\_UNORM UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f9e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18f9e-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="18f9e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18f9e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f9e-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="18f9e-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="18f9e-109">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="18f9e-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f9e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18f9e-110">Return value</span></span>

<span data-ttu-id="18f9e-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="18f9e-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f9e-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="18f9e-112">Requirements</span></span>



| <span data-ttu-id="18f9e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18f9e-113">Requirement</span></span> | <span data-ttu-id="18f9e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="18f9e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f9e-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="18f9e-115">Header</span></span><br/> | <dl> <span data-ttu-id="18f9e-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="18f9e-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18f9e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18f9e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f9e-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="18f9e-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="18f9e-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="18f9e-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





