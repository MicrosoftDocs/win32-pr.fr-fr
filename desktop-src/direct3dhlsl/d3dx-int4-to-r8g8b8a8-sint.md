---
title: D3DX_INT4_to_R8G8B8A8_SINT fonction)
description: Recompresse le XMINT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ Saint-le.
ms.assetid: ab9c5454-1673-43a9-ab76-bcd7b510b9a8
keywords:
- D3DX_INT4_to_R8G8B8A8_SINT fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_INT4_to_R8G8B8A8_SINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df4e4094ac96e7da2ccbff1da08e7aa1f7c4de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992153"
---
# <a name="d3dx_int4_to_r8g8b8a8_sint-function"></a><span data-ttu-id="2a686-104">D3DX \_ INT4 \_ à \_ la \_ fonction R8G8B8A8 Saint</span><span class="sxs-lookup"><span data-stu-id="2a686-104">D3DX\_INT4\_to\_R8G8B8A8\_SINT function</span></span>

<span data-ttu-id="2a686-105">Recompresse le XMINT4 donné dans un \_ format dxgi \_ R8G8B8A8 \_ Saint-le.</span><span class="sxs-lookup"><span data-stu-id="2a686-105">Packs the given XMINT4 back into a DXGI\_FORMAT\_R8G8B8A8\_SINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a686-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a686-106">Syntax</span></span>

``` syntax
UINT D3DX_INT4_to_R8G8B8A8_SINT(
   hlsl_precise XMINT4 unpackedInput
);
```

## <a name="parameters"></a><span data-ttu-id="2a686-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a686-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a686-108">*unpackedInput*</span><span class="sxs-lookup"><span data-stu-id="2a686-108">*unpackedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="2a686-109">Données du nuanceur à compresser.</span><span class="sxs-lookup"><span data-stu-id="2a686-109">The shader data to pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a686-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a686-110">Return value</span></span>

<span data-ttu-id="2a686-111">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="2a686-111">The packed shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a686-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2a686-112">Requirements</span></span>



| <span data-ttu-id="2a686-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a686-113">Requirement</span></span> | <span data-ttu-id="2a686-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a686-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a686-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a686-115">Header</span></span><br/> | <dl> <span data-ttu-id="2a686-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="2a686-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a686-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a686-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a686-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="2a686-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="2a686-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="2a686-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





