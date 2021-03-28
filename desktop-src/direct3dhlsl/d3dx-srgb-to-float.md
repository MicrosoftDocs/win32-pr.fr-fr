---
title: D3DX_SRGB_to_FLOAT fonction)
description: Convertit une valeur sRVB en valeur FLOAT. | D3DX_SRGB_to_FLOAT fonction)
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- D3DX_SRGB_to_FLOAT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953883"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="08d4f-105">\_ \_ Fonction de D3DX sRVB en \_ float</span><span class="sxs-lookup"><span data-stu-id="08d4f-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="08d4f-106">Convertit une valeur sRVB en valeur FLOAT.</span><span class="sxs-lookup"><span data-stu-id="08d4f-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d4f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08d4f-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="08d4f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08d4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d4f-109">*multiples*</span><span class="sxs-lookup"><span data-stu-id="08d4f-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="08d4f-110">Valeur sRVB à convertir.</span><span class="sxs-lookup"><span data-stu-id="08d4f-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d4f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08d4f-111">Return value</span></span>

<span data-ttu-id="08d4f-112">Valeur sRVB convertie.</span><span class="sxs-lookup"><span data-stu-id="08d4f-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d4f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="08d4f-113">Requirements</span></span>



| <span data-ttu-id="08d4f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08d4f-114">Requirement</span></span> | <span data-ttu-id="08d4f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08d4f-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d4f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="08d4f-116">Header</span></span><br/> | <dl> <span data-ttu-id="08d4f-117"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="08d4f-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d4f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08d4f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d4f-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="08d4f-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="08d4f-120">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="08d4f-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





