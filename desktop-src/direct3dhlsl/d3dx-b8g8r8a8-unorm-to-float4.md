---
title: D3DX_B8G8R8A8_UNORM_to_FLOAT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8A8 UNORM dans un XMFLOAT4.
ms.assetid: 1a52058c-825d-4607-b67d-8226dccdee54
keywords:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_B8G8R8A8_UNORM_to_FLOAT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6bca17f350d40b1f74884232da9d1250bdb0abd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974454"
---
# <a name="d3dx_b8g8r8a8_unorm_to_float4-function"></a><span data-ttu-id="98366-104">D3DX \_ B8G8R8A8 \_ UNORM \_ to \_ float4, fonction</span><span class="sxs-lookup"><span data-stu-id="98366-104">D3DX\_B8G8R8A8\_UNORM\_to\_FLOAT4 function</span></span>

<span data-ttu-id="98366-105">Décompresse les \_ \_ \_ données de nuanceur de format dxgi B8G8R8A8 UNORM dans un XMFLOAT4.</span><span class="sxs-lookup"><span data-stu-id="98366-105">Unpacks DXGI\_FORMAT\_B8G8R8A8\_UNORM shader data to an XMFLOAT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="98366-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98366-106">Syntax</span></span>

``` syntax
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="98366-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98366-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98366-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="98366-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="98366-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="98366-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98366-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98366-110">Return value</span></span>

<span data-ttu-id="98366-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="98366-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="98366-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="98366-112">Requirements</span></span>



| <span data-ttu-id="98366-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98366-113">Requirement</span></span> | <span data-ttu-id="98366-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="98366-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98366-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="98366-115">Header</span></span><br/> | <dl> <span data-ttu-id="98366-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="98366-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98366-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98366-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98366-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="98366-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="98366-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="98366-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





