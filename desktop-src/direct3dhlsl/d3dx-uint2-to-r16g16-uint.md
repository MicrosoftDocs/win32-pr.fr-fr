---
title: D3DX_UINT2_to_R16G16_UINT fonction)
description: Recompresse le XMUINT2 donné dans un \_ format dxgi \_ R16G16 \_ uint.
ms.assetid: 1f8aef92-7f34-4020-8a7e-6204922fc6d4
keywords:
- D3DX_UINT2_to_R16G16_UINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT2_to_R16G16_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59a20b62fc5d8078152ed483ae49afceeeda4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992196"
---
# <a name="d3dx_uint2_to_r16g16_uint-function"></a><span data-ttu-id="7af37-104">D3DX \_ UINT2 \_ à \_ R16G16 \_ uint, fonction</span><span class="sxs-lookup"><span data-stu-id="7af37-104">D3DX\_UINT2\_to\_R16G16\_UINT function</span></span>

<span data-ttu-id="7af37-105">Recompresse le XMUINT2 donné dans un \_ format dxgi \_ R16G16 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="7af37-105">Packs the given XMUINT2 back into a DXGI\_FORMAT\_R16G16\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af37-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7af37-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT2_to_R16G16_UINT(
   hlsl_precise XMUINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="7af37-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7af37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af37-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="7af37-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="7af37-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="7af37-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af37-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7af37-110">Return value</span></span>

<span data-ttu-id="7af37-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="7af37-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af37-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7af37-112">Requirements</span></span>



| <span data-ttu-id="7af37-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7af37-113">Requirement</span></span> | <span data-ttu-id="7af37-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7af37-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af37-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="7af37-115">Header</span></span><br/> | <dl> <span data-ttu-id="7af37-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="7af37-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af37-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7af37-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af37-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7af37-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="7af37-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="7af37-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





