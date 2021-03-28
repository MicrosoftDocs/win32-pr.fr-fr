---
title: D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format R8G8B8A8 UNORM dans un XMFLOAT4. | D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact fonction)
ms.assetid: ca7c2bf8-30fd-48fa-b4d9-e69c28c7f603
keywords:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d3d4a9d47eb520d151fe2e3388e99f401fc0a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953896"
---
# <a name="d3dx_r8g8b8a8_unorm_srgb_to_float4_inexact-function"></a><span data-ttu-id="17b04-105">D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ à \_ float4 \_ fonction inexacte</span><span class="sxs-lookup"><span data-stu-id="17b04-105">D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4\_inexact function</span></span>

<span data-ttu-id="17b04-106">Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format R8G8B8A8 UNORM dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="17b04-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b04-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17b04-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="17b04-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17b04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b04-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="17b04-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="17b04-110">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="17b04-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b04-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17b04-111">Return value</span></span>

<span data-ttu-id="17b04-112">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="17b04-112">The unpacked shader data.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b04-113">Notes</span><span class="sxs-lookup"><span data-stu-id="17b04-113">Remarks</span></span>

<span data-ttu-id="17b04-114">Cette fonction utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte.</span><span class="sxs-lookup"><span data-stu-id="17b04-114">This function uses shader instructions that don't have high enough precision to give the exact answer.</span></span> <span data-ttu-id="17b04-115">La fonction alternative [**D3DX \_ R8G8B8A8 \_ UNORM \_ sRVB \_ à \_ float4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) utilise une table de recherche stockée dans le nuanceur pour fournir une conversion d’sRGB en float exacte.</span><span class="sxs-lookup"><span data-stu-id="17b04-115">The alternative function [**D3DX\_R8G8B8A8\_UNORM\_SRGB\_to\_FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md) uses a lookup table stored in the shader to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b04-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="17b04-116">Requirements</span></span>



| <span data-ttu-id="17b04-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b04-117">Requirement</span></span> | <span data-ttu-id="17b04-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b04-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b04-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="17b04-119">Header</span></span><br/> | <dl> <span data-ttu-id="17b04-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="17b04-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b04-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17b04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b04-122">Fonctions</span><span class="sxs-lookup"><span data-stu-id="17b04-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="17b04-123">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="17b04-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





