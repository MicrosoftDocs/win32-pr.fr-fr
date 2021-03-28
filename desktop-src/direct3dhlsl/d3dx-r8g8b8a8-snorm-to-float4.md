---
title: D3DX_R8G8B8A8_SNORM_to_FLOAT4 fonction)
description: Décompresse le \_ format dxgi \_ R8G8B8A8 \_ ronfler les données de nuanceur dans un XMFLOAT4.
ms.assetid: 2f2b9d5e-f4d0-470a-a4bb-b333d57f03e7
keywords:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a4153fa30f2792008ccc45bc3e16f5d404f33a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974522"
---
# <a name="d3dx_r8g8b8a8_snorm_to_float4-function"></a><span data-ttu-id="c4c10-104">D3DX \_ R8G8B8A8 \_ ronfler \_ à la \_ fonction float4</span><span class="sxs-lookup"><span data-stu-id="c4c10-104">D3DX\_R8G8B8A8\_SNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="c4c10-105">Décompresse le \_ format dxgi \_ R8G8B8A8 \_ ronfler les données de nuanceur dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="c4c10-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c10-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c10-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="c4c10-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4c10-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c10-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="c4c10-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c10-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="c4c10-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c10-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4c10-110">Return value</span></span>

<span data-ttu-id="c4c10-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="c4c10-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c10-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4c10-112">Requirements</span></span>



| <span data-ttu-id="c4c10-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4c10-113">Requirement</span></span> | <span data-ttu-id="c4c10-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4c10-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c10-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4c10-115">Header</span></span><br/> | <dl> <span data-ttu-id="c4c10-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="c4c10-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c10-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4c10-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c10-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="c4c10-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="c4c10-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="c4c10-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





