---
title: D3DX_R10G10B10A2_UINT_to_UINT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R10G10B10A2 uint dans un XMINT4.
ms.assetid: 47c4f11f-936a-46d5-9533-1a4f9fce6168
keywords:
- D3DX_R10G10B10A2_UINT_to_UINT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R10G10B10A2_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378b013ad077c787253b4a58f24082d1c64b416f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982490"
---
# <a name="d3dx_r10g10b10a2_uint_to_uint4-function"></a><span data-ttu-id="ea9bf-104">D3DX \_ R10G10B10A2 \_ uint \_ à la \_ fonction UINT4</span><span class="sxs-lookup"><span data-stu-id="ea9bf-104">D3DX\_R10G10B10A2\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="ea9bf-105">Décompresse les \_ \_ \_ données de nuanceur dxgi R10G10B10A2 uint dans un XMINT4.</span><span class="sxs-lookup"><span data-stu-id="ea9bf-105">Unpacks DXGI\_FORMAT\_R10G10B10A2\_UINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea9bf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea9bf-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R10G10B10A2_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="ea9bf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea9bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9bf-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="ea9bf-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ea9bf-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="ea9bf-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9bf-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea9bf-110">Return value</span></span>

<span data-ttu-id="ea9bf-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="ea9bf-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea9bf-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ea9bf-112">Requirements</span></span>



| <span data-ttu-id="ea9bf-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea9bf-113">Requirement</span></span> | <span data-ttu-id="ea9bf-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea9bf-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9bf-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea9bf-115">Header</span></span><br/> | <dl> <span data-ttu-id="ea9bf-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="ea9bf-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9bf-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea9bf-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9bf-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="ea9bf-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ea9bf-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="ea9bf-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





