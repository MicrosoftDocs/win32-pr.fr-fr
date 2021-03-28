---
title: D3DX_FLOAT_to_SRGB fonction)
description: Convertit une valeur FLOAT en un SRGB.
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- D3DX_FLOAT_to_SRGB fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996176"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="0e6e2-104">D3DX \_ float \_ to \_ sRGB, fonction</span><span class="sxs-lookup"><span data-stu-id="0e6e2-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="0e6e2-105">Convertit une valeur FLOAT en un SRGB.</span><span class="sxs-lookup"><span data-stu-id="0e6e2-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6e2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e6e2-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="0e6e2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e6e2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e6e2-108">*multiples*</span><span class="sxs-lookup"><span data-stu-id="0e6e2-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="0e6e2-109">Valeur FLOTTante à convertir.</span><span class="sxs-lookup"><span data-stu-id="0e6e2-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e6e2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e6e2-110">Return value</span></span>

<span data-ttu-id="0e6e2-111">Valeur sRVB convertie.</span><span class="sxs-lookup"><span data-stu-id="0e6e2-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e6e2-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e6e2-112">Requirements</span></span>



| <span data-ttu-id="0e6e2-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e6e2-113">Requirement</span></span> | <span data-ttu-id="0e6e2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e6e2-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e6e2-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e6e2-115">Header</span></span><br/> | <dl> <span data-ttu-id="0e6e2-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="0e6e2-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e6e2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e6e2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6e2-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="0e6e2-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="0e6e2-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="0e6e2-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





