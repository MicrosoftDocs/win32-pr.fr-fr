---
title: D3DX_R8G8B8A8_SINT_to_INT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R8G8B8A8 Saint vers un XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- D3DX_R8G8B8A8_SINT_to_INT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116246"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="5d6b2-104">D3DX \_ R8G8B8A8 \_ Saint \_ - \_ INT4 fonction</span><span class="sxs-lookup"><span data-stu-id="5d6b2-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="5d6b2-105">Décompresse les \_ \_ \_ données de nuanceur dxgi R8G8B8A8 Saint vers un XMINT4.</span><span class="sxs-lookup"><span data-stu-id="5d6b2-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6b2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d6b2-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5d6b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d6b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6b2-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="5d6b2-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6b2-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="5d6b2-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6b2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d6b2-110">Return value</span></span>

<span data-ttu-id="5d6b2-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="5d6b2-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d6b2-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d6b2-112">Requirements</span></span>



| <span data-ttu-id="5d6b2-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d6b2-113">Requirement</span></span> | <span data-ttu-id="5d6b2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d6b2-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d6b2-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d6b2-115">Header</span></span><br/> | <dl> <span data-ttu-id="5d6b2-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5d6b2-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d6b2-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d6b2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6b2-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="5d6b2-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5d6b2-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="5d6b2-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





