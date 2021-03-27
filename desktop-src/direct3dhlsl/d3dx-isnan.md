---
title: D3DX_IsNan fonction)
description: Détermine si la valeur est une valeur NaN (pas un nombre).
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953982"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="fbf9d-104">D3DX \_ isNaN, fonction</span><span class="sxs-lookup"><span data-stu-id="fbf9d-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="fbf9d-105">Détermine si la valeur est une valeur NaN (pas un nombre).</span><span class="sxs-lookup"><span data-stu-id="fbf9d-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf9d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbf9d-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="fbf9d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbf9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf9d-108">*\_V*</span><span class="sxs-lookup"><span data-stu-id="fbf9d-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="fbf9d-109">Valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fbf9d-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf9d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbf9d-110">Return value</span></span>

<span data-ttu-id="fbf9d-111">true si NaN ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="fbf9d-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf9d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fbf9d-112">Requirements</span></span>



| <span data-ttu-id="fbf9d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbf9d-113">Requirement</span></span> | <span data-ttu-id="fbf9d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbf9d-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf9d-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="fbf9d-115">Header</span></span><br/> | <dl> <span data-ttu-id="fbf9d-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fbf9d-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbf9d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbf9d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf9d-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="fbf9d-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fbf9d-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="fbf9d-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





