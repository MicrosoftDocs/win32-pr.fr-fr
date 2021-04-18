---
title: D3DX_SRGB_to_FLOAT_inexact fonction)
description: Convertit une valeur sRVB en valeur FLOAT. | D3DX_SRGB_to_FLOAT_inexact fonction)
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974515"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="ad9e4-105">D3DX \_ sRVB \_ en \_ float, \_ fonction inexacte</span><span class="sxs-lookup"><span data-stu-id="ad9e4-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="ad9e4-106">Convertit une valeur sRVB en valeur FLOAT.</span><span class="sxs-lookup"><span data-stu-id="ad9e4-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad9e4-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="ad9e4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad9e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9e4-109">*multiples*</span><span class="sxs-lookup"><span data-stu-id="ad9e4-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="ad9e4-110">Valeur sRVB à convertir.</span><span class="sxs-lookup"><span data-stu-id="ad9e4-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9e4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad9e4-111">Return value</span></span>

<span data-ttu-id="ad9e4-112">Valeur sRVB convertie.</span><span class="sxs-lookup"><span data-stu-id="ad9e4-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9e4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ad9e4-113">Remarks</span></span>

<span data-ttu-id="ad9e4-114">Cette fonction n’a pas une précision suffisamment élevée pour fournir la réponse exacte.</span><span class="sxs-lookup"><span data-stu-id="ad9e4-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="ad9e4-115">La fonction alternative de [**D3DX \_ sRVB \_ en \_ float**](d3dx-srgb-to-float.md) utilise une table de recherche pour fournir une conversion d’sRVB en valeurs flottantes exacte.</span><span class="sxs-lookup"><span data-stu-id="ad9e4-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9e4-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad9e4-116">Requirements</span></span>



| <span data-ttu-id="ad9e4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad9e4-117">Requirement</span></span> | <span data-ttu-id="ad9e4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad9e4-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9e4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad9e4-119">Header</span></span><br/> | <dl> <span data-ttu-id="ad9e4-120"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="ad9e4-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad9e4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad9e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9e4-122">Fonctions</span><span class="sxs-lookup"><span data-stu-id="ad9e4-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ad9e4-123">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="ad9e4-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





