---
title: D3DX_INT2_to_R16G16_SINT fonction)
description: Recompresse le XMINT2 donné dans un \_ format dxgi \_ R16G16 \_ Saint-le.
ms.assetid: dc37e8a3-31d4-4af6-9bc3-9aa5062c066a
keywords:
- D3DX_INT2_to_R16G16_SINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_INT2_to_R16G16_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97d60ba29b2451dea973b4ec0453f3a4df2ecdd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982530"
---
# <a name="d3dx_int2_to_r16g16_sint-function"></a><span data-ttu-id="e8a13-104">D3DX \_ Int2 \_ à \_ la \_ fonction R16G16 Saint</span><span class="sxs-lookup"><span data-stu-id="e8a13-104">D3DX\_INT2\_to\_R16G16\_SINT function</span></span>

<span data-ttu-id="e8a13-105">Recompresse le XMINT2 donné dans un \_ format dxgi \_ R16G16 \_ Saint-le.</span><span class="sxs-lookup"><span data-stu-id="e8a13-105">Packs the given XMINT2 back into a DXGI\_FORMAT\_R16G16\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a13-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8a13-106">Syntax</span></span>

``` syntax
UINT D3DX_INT2_to_R16G16_SINT(
   hlsl_precise XMINT2 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="e8a13-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8a13-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a13-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="e8a13-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a13-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="e8a13-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a13-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8a13-110">Return value</span></span>

<span data-ttu-id="e8a13-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="e8a13-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a13-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e8a13-112">Requirements</span></span>



| <span data-ttu-id="e8a13-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8a13-113">Requirement</span></span> | <span data-ttu-id="e8a13-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8a13-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a13-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8a13-115">Header</span></span><br/> | <dl> <span data-ttu-id="e8a13-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="e8a13-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a13-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8a13-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a13-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="e8a13-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="e8a13-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="e8a13-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





