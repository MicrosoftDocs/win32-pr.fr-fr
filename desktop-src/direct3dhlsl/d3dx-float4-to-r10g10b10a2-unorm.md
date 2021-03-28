---
title: D3DX_FLOAT4_to_R10G10B10A2_UNORM fonction)
description: Recompresse le XMFLOAT4 donné dans un \_ UNORM de format dxgi \_ R10G10B10A2 \_ .
ms.assetid: 20471435-bb1a-4151-a03a-c334b2a7d944
keywords:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R10G10B10A2_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c8d80b8822d03a43e813226c28dde8693397a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974435"
---
# <a name="d3dx_float4_to_r10g10b10a2_unorm-function"></a><span data-ttu-id="dc477-104">D3DX \_ float4 \_ vers \_ R10G10B10A2 \_ UNORM, fonction</span><span class="sxs-lookup"><span data-stu-id="dc477-104">D3DX\_FLOAT4\_to\_R10G10B10A2\_UNORM function</span></span>

<span data-ttu-id="dc477-105">Recompresse le XMFLOAT4 donné dans un \_ UNORM de format dxgi \_ R10G10B10A2 \_ .</span><span class="sxs-lookup"><span data-stu-id="dc477-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R10G10B10A2\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc477-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc477-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="dc477-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc477-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc477-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="dc477-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="dc477-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="dc477-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc477-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc477-110">Return value</span></span>

<span data-ttu-id="dc477-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="dc477-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc477-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dc477-112">Requirements</span></span>



| <span data-ttu-id="dc477-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc477-113">Requirement</span></span> | <span data-ttu-id="dc477-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc477-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc477-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc477-115">Header</span></span><br/> | <dl> <span data-ttu-id="dc477-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="dc477-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc477-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc477-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc477-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="dc477-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="dc477-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="dc477-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





