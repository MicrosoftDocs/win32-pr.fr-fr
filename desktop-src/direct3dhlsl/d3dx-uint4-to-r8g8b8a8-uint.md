---
title: D3DX_UINT4_to_R8G8B8A8_UINT fonction)
description: Recompresse le XMUINT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ uint.
ms.assetid: d4770dfc-1387-40c3-a4f8-365a1421fa3c
keywords:
- D3DX_UINT4_to_R8G8B8A8_UINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_UINT4_to_R8G8B8A8_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef8128d2d1989e986d8ff11e2d7e42e85f1fbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992192"
---
# <a name="d3dx_uint4_to_r8g8b8a8_uint-function"></a><span data-ttu-id="fd88c-104">D3DX \_ UINT4 \_ à \_ R8G8B8A8 \_ uint, fonction</span><span class="sxs-lookup"><span data-stu-id="fd88c-104">D3DX\_UINT4\_to\_R8G8B8A8\_UINT function</span></span>

<span data-ttu-id="fd88c-105">Recompresse le XMUINT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="fd88c-105">Packs the given XMUINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd88c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd88c-106">Syntax</span></span>

``` syntax
UINT D3DX_UINT4_to_R8G8B8A8_UINT(
   hlsl_precise XMUINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="fd88c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd88c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd88c-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="fd88c-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="fd88c-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="fd88c-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd88c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fd88c-110">Return value</span></span>

<span data-ttu-id="fd88c-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="fd88c-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd88c-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fd88c-112">Requirements</span></span>



| <span data-ttu-id="fd88c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd88c-113">Requirement</span></span> | <span data-ttu-id="fd88c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd88c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd88c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd88c-115">Header</span></span><br/> | <dl> <span data-ttu-id="fd88c-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="fd88c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd88c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd88c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd88c-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="fd88c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="fd88c-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="fd88c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





