---
title: D3DX_FLOAT_to_UINT fonction)
description: Convertit une valeur FLOAT en UINT.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322694"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="4bf30-104">D3DX \_ float \_ to \_ uint, fonction</span><span class="sxs-lookup"><span data-stu-id="4bf30-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="4bf30-105">Convertit une valeur FLOAT en UINT.</span><span class="sxs-lookup"><span data-stu-id="4bf30-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf30-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bf30-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="4bf30-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bf30-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf30-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="4bf30-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="4bf30-109">Vecteur v.</span><span class="sxs-lookup"><span data-stu-id="4bf30-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="4bf30-110">*\_Échelle*</span><span class="sxs-lookup"><span data-stu-id="4bf30-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="4bf30-111">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="4bf30-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf30-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4bf30-112">Return value</span></span>

<span data-ttu-id="4bf30-113">Valeur FLOAT convertie</span><span class="sxs-lookup"><span data-stu-id="4bf30-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf30-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4bf30-114">Requirements</span></span>



| <span data-ttu-id="4bf30-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bf30-115">Requirement</span></span> | <span data-ttu-id="4bf30-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bf30-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf30-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bf30-117">Header</span></span><br/> | <dl> <span data-ttu-id="4bf30-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="4bf30-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bf30-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bf30-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf30-120">Fonctions</span><span class="sxs-lookup"><span data-stu-id="4bf30-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="4bf30-121">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="4bf30-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





