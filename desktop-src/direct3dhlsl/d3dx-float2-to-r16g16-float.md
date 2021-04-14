---
title: D3DX_FLOAT2_to_R16G16_FLOAT fonction)
description: Recompresse le XMFLOAT2 donné dans un \_ format dxgi \_ R16G16 \_ float.
ms.assetid: 8d03fac3-68f0-4c85-afaa-ff2cb76f1b73
keywords:
- D3DX_FLOAT2_to_R16G16_FLOAT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT2_to_R16G16_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849eb4dde5ab11e98675a1581519aabbeeb1e8da
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992129"
---
# <a name="d3dx_float2_to_r16g16_float-function"></a><span data-ttu-id="3a881-104">D3DX \_ FLOAT2 \_ vers \_ R16G16 \_ float, fonction</span><span class="sxs-lookup"><span data-stu-id="3a881-104">D3DX\_FLOAT2\_to\_R16G16\_FLOAT function</span></span>

<span data-ttu-id="3a881-105">Recompresse le XMFLOAT2 donné dans un \_ format dxgi \_ R16G16 \_ float.</span><span class="sxs-lookup"><span data-stu-id="3a881-105">Packs the given XMFLOAT2 back into a DXGI\_FORMAT\_R16G16\_FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a881-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a881-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT2_to_R16G16_FLOAT(
   XMFLOAT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="3a881-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a881-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a881-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="3a881-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3a881-109">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="3a881-109">The unpacked shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a881-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a881-110">Return value</span></span>

<span data-ttu-id="3a881-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="3a881-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a881-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a881-112">Requirements</span></span>



| <span data-ttu-id="3a881-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a881-113">Requirement</span></span> | <span data-ttu-id="3a881-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a881-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a881-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a881-115">Header</span></span><br/> | <dl> <span data-ttu-id="3a881-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="3a881-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a881-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a881-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a881-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="3a881-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="3a881-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="3a881-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





