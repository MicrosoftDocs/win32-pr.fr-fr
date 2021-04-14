---
title: D3DX_FLOAT4_to_R8G8B8A8_SNORM fonction)
description: Recompresse le XMFLOAT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ ronfler.
ms.assetid: 425aeabd-6249-4777-8935-827691abef24
keywords:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT4_to_R8G8B8A8_SNORM
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194835ef126a3441dc2b842784dfa841ae1d7d6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323289"
---
# <a name="d3dx_float4_to_r8g8b8a8_snorm-function"></a><span data-ttu-id="23cac-104">D3DX \_ float4 \_ à \_ R8G8B8A8 \_ ronfler, fonction</span><span class="sxs-lookup"><span data-stu-id="23cac-104">D3DX\_FLOAT4\_to\_R8G8B8A8\_SNORM function</span></span>

<span data-ttu-id="23cac-105">Recompresse le XMFLOAT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ ronfler.</span><span class="sxs-lookup"><span data-stu-id="23cac-105">Packs the given XMFLOAT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SNORM.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23cac-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT4_to_R8G8B8A8_SNORM(
   hlsl_precise XMFLOAT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="23cac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23cac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23cac-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="23cac-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="23cac-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="23cac-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23cac-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23cac-110">Return value</span></span>

<span data-ttu-id="23cac-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="23cac-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="23cac-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23cac-112">Requirements</span></span>



| <span data-ttu-id="23cac-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23cac-113">Requirement</span></span> | <span data-ttu-id="23cac-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="23cac-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23cac-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="23cac-115">Header</span></span><br/> | <dl> <span data-ttu-id="23cac-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="23cac-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23cac-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23cac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23cac-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="23cac-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="23cac-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="23cac-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





