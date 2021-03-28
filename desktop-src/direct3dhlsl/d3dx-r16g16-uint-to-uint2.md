---
title: D3DX_R16G16_UINT_to_UINT2 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R16G16 uint dans un XMUINT2.
ms.assetid: bb24fdc4-db47-4cf3-af05-4b39c3af3701
keywords:
- D3DX_R16G16_UINT_to_UINT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_UINT_to_UINT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2586ff8876ee10368d49b816b38f5c9c8caf7c7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322594"
---
# <a name="d3dx_r16g16_uint_to_uint2-function"></a><span data-ttu-id="40c4a-104">D3DX \_ R16G16 \_ uint \_ à la \_ fonction UINT2</span><span class="sxs-lookup"><span data-stu-id="40c4a-104">D3DX\_R16G16\_UINT\_to\_UINT2 function</span></span>

<span data-ttu-id="40c4a-105">Décompresse les \_ \_ \_ données de nuanceur dxgi R16G16 uint dans un XMUINT2.</span><span class="sxs-lookup"><span data-stu-id="40c4a-105">Unpacks DXGI\_FORMAT\_R16G16\_UINT shader data to an XMUINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c4a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40c4a-106">Syntax</span></span>

``` syntax
XMUINT2 D3DX_R16G16_UINT_to_UINT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="40c4a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40c4a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c4a-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="40c4a-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="40c4a-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="40c4a-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c4a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40c4a-110">Return value</span></span>

<span data-ttu-id="40c4a-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="40c4a-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c4a-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="40c4a-112">Requirements</span></span>



| <span data-ttu-id="40c4a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40c4a-113">Requirement</span></span> | <span data-ttu-id="40c4a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="40c4a-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c4a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="40c4a-115">Header</span></span><br/> | <dl> <span data-ttu-id="40c4a-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="40c4a-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c4a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c4a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c4a-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="40c4a-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="40c4a-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="40c4a-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





