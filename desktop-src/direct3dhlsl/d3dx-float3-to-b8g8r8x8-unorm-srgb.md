---
title: D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB fonction)
description: Recompresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM \_ sRVB.
ms.assetid: 42d1e8f1-d1b7-4c93-a658-d25790e78830
keywords:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e74dd5fbc1329d884968d76039061fceb22aafbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992176"
---
# <a name="d3dx_float3_to_b8g8r8x8_unorm_srgb-function"></a><span data-ttu-id="2cd48-104">D3DX \_ FLOAT3 \_ to \_ B8G8R8X8 \_ UNORM \_ sRGB, fonction</span><span class="sxs-lookup"><span data-stu-id="2cd48-104">D3DX\_FLOAT3\_to\_B8G8R8X8\_UNORM\_SRGB function</span></span>

<span data-ttu-id="2cd48-105">Recompresse le XMFLOAT3 donné dans un \_ format dxgi \_ B8G8R8X8 \_ UNORM \_ sRVB.</span><span class="sxs-lookup"><span data-stu-id="2cd48-105">Packs the given XMFLOAT3 back into a DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd48-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cd48-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(
   hlsl_precise XMFLOAT3 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="2cd48-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2cd48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd48-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="2cd48-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2cd48-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="2cd48-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd48-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2cd48-110">Return value</span></span>

<span data-ttu-id="2cd48-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="2cd48-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd48-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2cd48-112">Requirements</span></span>



| <span data-ttu-id="2cd48-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cd48-113">Requirement</span></span> | <span data-ttu-id="2cd48-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd48-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd48-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2cd48-115">Header</span></span><br/> | <dl> <span data-ttu-id="2cd48-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="2cd48-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd48-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cd48-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd48-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="2cd48-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2cd48-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="2cd48-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





