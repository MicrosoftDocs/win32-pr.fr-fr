---
title: D3DX_FLOAT2_to_R16G16_UNORM fonction)
description: Recompresse le XMFLOAT2 donné dans un \_ UNORM de format dxgi \_ R16G16 \_ .
ms.assetid: 5a1bd034-262f-4f55-8f38-d2fda42bb13b
keywords:
- D3DX_FLOAT2_to_R16G16_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0a6ffe3081955db79765d80278394eb89ab188
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992209"
---
# <a name="d3dx_float2_to_r16g16_unorm-function"></a><span data-ttu-id="87a71-104">D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ UNORM, fonction</span><span class="sxs-lookup"><span data-stu-id="87a71-104">D3DX\_FLOAT2\_to\_R16G16\_UNORM function</span></span>

<span data-ttu-id="87a71-105">Recompresse le XMFLOAT2 donné dans un \_ UNORM de format dxgi \_ R16G16 \_ .</span><span class="sxs-lookup"><span data-stu-id="87a71-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a71-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87a71-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_UNORM(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="87a71-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87a71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a71-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="87a71-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="87a71-109">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="87a71-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a71-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87a71-110">Return value</span></span>

<span data-ttu-id="87a71-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="87a71-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="87a71-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="87a71-112">Requirements</span></span>



| <span data-ttu-id="87a71-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87a71-113">Requirement</span></span> | <span data-ttu-id="87a71-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="87a71-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a71-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="87a71-115">Header</span></span><br/> | <dl> <span data-ttu-id="87a71-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="87a71-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a71-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87a71-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a71-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="87a71-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="87a71-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="87a71-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





