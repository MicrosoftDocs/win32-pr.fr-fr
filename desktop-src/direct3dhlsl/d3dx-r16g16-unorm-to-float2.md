---
title: D3DX_R16G16_UNORM_to_FLOAT2 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi R16G16 UNORM dans un XMFLOAT2.
ms.assetid: e82e2a47-f494-4085-8c02-1bac3088d29f
keywords:
- D3DX_R16G16_UNORM_to_FLOAT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UNORM_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba4ca1bb02e66289ec66d0ec4f58978800f6538
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322798"
---
# <a name="d3dx_r16g16_unorm_to_float2-function"></a><span data-ttu-id="8ebe6-104">D3DX \_ R16G16 \_ UNORM \_ to \_ FLOAT2, fonction</span><span class="sxs-lookup"><span data-stu-id="8ebe6-104">D3DX\_R16G16\_UNORM\_to\_FLOAT2 function</span></span>

<span data-ttu-id="8ebe6-105">Décompresse les \_ \_ \_ données de nuanceur de format dxgi R16G16 UNORM dans un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="8ebe6-105">Unpacks DXGI\_FORMAT\_R16G16\_UNORM shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebe6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ebe6-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8ebe6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ebe6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ebe6-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="8ebe6-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8ebe6-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="8ebe6-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ebe6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ebe6-110">Return value</span></span>

<span data-ttu-id="8ebe6-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="8ebe6-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ebe6-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8ebe6-112">Requirements</span></span>



| <span data-ttu-id="8ebe6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ebe6-113">Requirement</span></span> | <span data-ttu-id="8ebe6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ebe6-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebe6-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ebe6-115">Header</span></span><br/> | <dl> <span data-ttu-id="8ebe6-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8ebe6-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ebe6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ebe6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ebe6-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="8ebe6-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8ebe6-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="8ebe6-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





