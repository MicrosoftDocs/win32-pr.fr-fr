---
title: D3DX_R16G16_FLOAT_to_FLOAT2 fonction)
description: Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT2.
ms.assetid: 6c57dc86-d034-4b54-8572-44ac3738beb9
keywords:
- D3DX_R16G16_FLOAT_to_FLOAT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_FLOAT_to_FLOAT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6fb721e59a63415f98216b6e3f81a92e7598f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116278"
---
# <a name="d3dx_r16g16_float_to_float2-function"></a><span data-ttu-id="d4cc1-104">D3DX \_ R16G16 \_ float \_ to \_ FLOAT2, fonction</span><span class="sxs-lookup"><span data-stu-id="d4cc1-104">D3DX\_R16G16\_FLOAT\_to\_FLOAT2 function</span></span>

<span data-ttu-id="d4cc1-105">Décompresse les \_ \_ \_ \_ données de nuanceur dxgi de format B8G8R8X8 UNORM dans un XMFLOAT2.</span><span class="sxs-lookup"><span data-stu-id="d4cc1-105">Unpacks DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB shader data to an XMFLOAT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cc1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4cc1-106">Syntax</span></span>

``` syntax
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="d4cc1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4cc1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4cc1-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="d4cc1-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="d4cc1-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="d4cc1-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4cc1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4cc1-110">Return value</span></span>

<span data-ttu-id="d4cc1-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="d4cc1-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4cc1-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d4cc1-112">Requirements</span></span>



| <span data-ttu-id="d4cc1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4cc1-113">Requirement</span></span> | <span data-ttu-id="d4cc1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4cc1-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cc1-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4cc1-115">Header</span></span><br/> | <dl> <span data-ttu-id="d4cc1-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="d4cc1-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4cc1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4cc1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4cc1-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="d4cc1-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="d4cc1-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="d4cc1-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





