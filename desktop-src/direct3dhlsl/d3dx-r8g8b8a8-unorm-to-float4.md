---
title: D3DX_R8G8B8A8_UNORM_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi R8G8B8A8 UNORM dans un XMFLOAT4. | D3DX_R8G8B8A8_UNORM_to_FLOAT4 fonction)
ms.assetid: 94430f29-4872-4ecd-99b9-72f3b77c47f2
keywords:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e24b9f29d2e54f62582407e8ad40488032f8a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322797"
---
# <a name="d3dx_r8g8b8a8_unorm_to_float4-function"></a><span data-ttu-id="f64bf-105">D3DX \_ R8G8B8A8 \_ UNORM \_ to \_ float4, fonction</span><span class="sxs-lookup"><span data-stu-id="f64bf-105">D3DX\_R8G8B8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="f64bf-106">Décompresse les \_ \_ \_ données de nuanceur de format dxgi R8G8B8A8 UNORM dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="f64bf-106">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="f64bf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f64bf-107">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="f64bf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f64bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f64bf-109">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="f64bf-109">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="f64bf-110">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="f64bf-110">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f64bf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f64bf-111">Return value</span></span>

<span data-ttu-id="f64bf-112">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="f64bf-112">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f64bf-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f64bf-113">Requirements</span></span>



| <span data-ttu-id="f64bf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f64bf-114">Requirement</span></span> | <span data-ttu-id="f64bf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f64bf-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f64bf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="f64bf-116">Header</span></span><br/> | <dl> <span data-ttu-id="f64bf-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="f64bf-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f64bf-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f64bf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f64bf-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="f64bf-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="f64bf-120">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="f64bf-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





