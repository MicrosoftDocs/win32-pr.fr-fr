---
title: D3DX_FLOAT4_to_R8G8B8A8_UNORM fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi R8G8B8A8 UNORM dans un XMFLOAT4. | D3DX_FLOAT4_to_R8G8B8A8_UNORM fonction)
ms.assetid: c589c1e5-24ee-4fd7-b18d-5ede52f9f05d
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 603fa1e887ed54e62502b70602e89f97c7cdffa0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762325"
---
# <a name="d3dx_float4_to_r8g8b8a8_unorm-function"></a><span data-ttu-id="bc606-105">D3DX \_ float4 \_ vers \_ R8G8B8A8 \_ UNORM, fonction</span><span class="sxs-lookup"><span data-stu-id="bc606-105">D3DX\_FLOAT4\_to\_R8G8B8A8\_UNORM function</span></span>

<span data-ttu-id="bc606-106">Décompresse les \_ \_ \_ données de nuanceur de format dxgi R8G8B8A8 UNORM dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="bc606-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc606-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc606-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_FLOAT4_to_R8G8B8A8_UNORM(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="bc606-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc606-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc606-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="bc606-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="bc606-110">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="bc606-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc606-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc606-111">Return value</span></span>

<span data-ttu-id="bc606-112">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="bc606-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc606-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc606-113">Requirements</span></span>



| <span data-ttu-id="bc606-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc606-114">Requirement</span></span> | <span data-ttu-id="bc606-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc606-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc606-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc606-116">Header</span></span><br/> | <dl> <span data-ttu-id="bc606-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="bc606-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc606-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc606-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc606-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="bc606-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="bc606-120">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="bc606-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





