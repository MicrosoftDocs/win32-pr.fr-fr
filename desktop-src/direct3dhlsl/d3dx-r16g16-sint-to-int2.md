---
title: D3DX_R16G16_SINT_to_INT2 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R16G16 Saint vers un XMINT2.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- D3DX_R16G16_SINT_to_INT2 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996152"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="671aa-104">D3DX \_ R16G16 \_ Saint \_ - \_ Int2 fonction</span><span class="sxs-lookup"><span data-stu-id="671aa-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="671aa-105">Décompresse les \_ \_ \_ données de nuanceur dxgi R16G16 Saint vers un XMINT2.</span><span class="sxs-lookup"><span data-stu-id="671aa-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="671aa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="671aa-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="671aa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="671aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671aa-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="671aa-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="671aa-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="671aa-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671aa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="671aa-110">Return value</span></span>

<span data-ttu-id="671aa-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="671aa-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="671aa-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="671aa-112">Requirements</span></span>



| <span data-ttu-id="671aa-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="671aa-113">Requirement</span></span> | <span data-ttu-id="671aa-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="671aa-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671aa-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="671aa-115">Header</span></span><br/> | <dl> <span data-ttu-id="671aa-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="671aa-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671aa-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="671aa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671aa-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="671aa-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="671aa-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="671aa-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





