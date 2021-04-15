---
title: D3DX_R16G16_SNORM_to_FLOAT2 fonction)
description: Décompresse le \_ format dxgi \_ R16G16 \_ ronfler les données de nuanceur dans un XMFLOAT2.
ms.assetid: b54df555-b71f-46cd-8be7-34de785d15e2
keywords:
- D3DX_R16G16_SNORM_to_FLOAT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3d45f486d2c44e2cbe319e920ab4bdec764fd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992205"
---
# <a name="d3dx_r16g16_snorm_to_float2-function"></a><span data-ttu-id="921b4-104">D3DX \_ R16G16 \_ ronfler \_ à la \_ fonction FLOAT2</span><span class="sxs-lookup"><span data-stu-id="921b4-104">D3DX\_R16G16\_SNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="921b4-105">Décompresse le \_ format dxgi \_ R16G16 \_ ronfler les données de nuanceur dans un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="921b4-105">Unpacks DXGI\_FORMAT\_R16G16\_SNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="921b4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="921b4-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="921b4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="921b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="921b4-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="921b4-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="921b4-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="921b4-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="921b4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="921b4-110">Return value</span></span>

<span data-ttu-id="921b4-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="921b4-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="921b4-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="921b4-112">Requirements</span></span>



| <span data-ttu-id="921b4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="921b4-113">Requirement</span></span> | <span data-ttu-id="921b4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="921b4-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921b4-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="921b4-115">Header</span></span><br/> | <dl> <span data-ttu-id="921b4-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="921b4-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921b4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="921b4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921b4-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="921b4-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="921b4-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="921b4-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





