---
title: D3DX_FLOAT2_to_R16G16_SNORM fonction)
description: Recompresse le XMFLOAT2 donné dans un \_ format dxgi \_ R16G16 \_ ronfler.
ms.assetid: 7c5c6aae-b750-435a-9582-18b7689bc2d9
keywords:
- D3DX_FLOAT2_to_R16G16_SNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63d7d7f03988e416d06b645e5c15163e431a7e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953884"
---
# <a name="d3dx_float2_to_r16g16_snorm-function"></a><span data-ttu-id="6d9b8-104">D3DX \_ FLOAT2 \_ à \_ R16G16 \_ ronfler, fonction</span><span class="sxs-lookup"><span data-stu-id="6d9b8-104">D3DX\_FLOAT2\_to\_R16G16\_SNORM function</span></span>

<span data-ttu-id="6d9b8-105">Recompresse le XMFLOAT2 donné dans un \_ format dxgi \_ R16G16 \_ ronfler.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d9b8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d9b8-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_SNORM(
   hlsl_precise XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="6d9b8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d9b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d9b8-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="6d9b8-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="6d9b8-109">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d9b8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d9b8-110">Return value</span></span>

<span data-ttu-id="6d9b8-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="6d9b8-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d9b8-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d9b8-112">Requirements</span></span>



| <span data-ttu-id="6d9b8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d9b8-113">Requirement</span></span> | <span data-ttu-id="6d9b8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d9b8-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9b8-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d9b8-115">Header</span></span><br/> | <dl> <span data-ttu-id="6d9b8-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="6d9b8-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d9b8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d9b8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d9b8-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="6d9b8-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="6d9b8-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="6d9b8-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





