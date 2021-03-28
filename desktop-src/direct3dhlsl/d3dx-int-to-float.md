---
title: D3DX_INT_to_FLOAT fonction)
description: Convertit une valeur INT en valeur FLOAT.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982498"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="805c9-104">D3DX \_ int \_ to \_ float, fonction</span><span class="sxs-lookup"><span data-stu-id="805c9-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="805c9-105">Convertit une valeur INT en valeur FLOAT.</span><span class="sxs-lookup"><span data-stu-id="805c9-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="805c9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="805c9-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="805c9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805c9-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="805c9-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="805c9-109">Valeur v.</span><span class="sxs-lookup"><span data-stu-id="805c9-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="805c9-110">*\_Échelle*</span><span class="sxs-lookup"><span data-stu-id="805c9-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="805c9-111">Valeur de mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="805c9-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805c9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="805c9-112">Return value</span></span>

<span data-ttu-id="805c9-113">Valeur int convertie.</span><span class="sxs-lookup"><span data-stu-id="805c9-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="805c9-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="805c9-114">Requirements</span></span>



| <span data-ttu-id="805c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="805c9-115">Requirement</span></span> | <span data-ttu-id="805c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="805c9-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805c9-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="805c9-117">Header</span></span><br/> | <dl> <span data-ttu-id="805c9-118"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="805c9-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805c9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="805c9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805c9-120">Fonctions</span><span class="sxs-lookup"><span data-stu-id="805c9-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="805c9-121">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="805c9-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





