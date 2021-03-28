---
title: D3DX_FLOAT4_to_B8G8R8A8_UNORM fonction)
description: Recompresse le XMFLOAT4 donné dans un \_ UNORM de format dxgi \_ B8G8R8A8 \_ .
ms.assetid: 5b7452ed-446a-4760-83e6-f3209ac8daf4
keywords:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_B8G8R8A8_UNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddec0922218b9770d7a0c4cb4877f6144eded900
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974507"
---
# <a name="d3dx_float4_to_b8g8r8a8_unorm-function"></a><span data-ttu-id="354b9-104">D3DX \_ float4 \_ vers \_ B8G8R8A8 \_ UNORM, fonction</span><span class="sxs-lookup"><span data-stu-id="354b9-104">D3DX\_FLOAT4\_to\_B8G8R8A8\_UNORM function</span></span>

<span data-ttu-id="354b9-105">Recompresse le XMFLOAT4 donné dans un \_ UNORM de format dxgi \_ B8G8R8A8 \_ .</span><span class="sxs-lookup"><span data-stu-id="354b9-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_B8G8R8A8\_UNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="354b9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="354b9-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_B8G8R8A8_UNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="354b9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="354b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354b9-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="354b9-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="354b9-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="354b9-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354b9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="354b9-110">Return value</span></span>

<span data-ttu-id="354b9-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="354b9-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="354b9-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="354b9-112">Requirements</span></span>



| <span data-ttu-id="354b9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="354b9-113">Requirement</span></span> | <span data-ttu-id="354b9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="354b9-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354b9-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="354b9-115">Header</span></span><br/> | <dl> <span data-ttu-id="354b9-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="354b9-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="354b9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="354b9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354b9-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="354b9-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="354b9-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="354b9-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





