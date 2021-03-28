---
title: D3DX_R8G8B8A8_UINT_to_UINT4 fonction)
description: Décompresse les \_ \_ \_ données de nuanceur dxgi R8G8B8A8 uint dans un XMUINT4.
ms.assetid: fe25041f-db18-4555-a77a-e8d487143aa6
keywords:
- D3DX_R8G8B8A8_UINT_to_UINT4 fonction HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_UINT_to_UINT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a371a36e797e1bff17aff457e11b140e4775894
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974518"
---
# <a name="d3dx_r8g8b8a8_uint_to_uint4-function"></a><span data-ttu-id="8948c-104">D3DX \_ R8G8B8A8 \_ uint \_ à la \_ fonction UINT4</span><span class="sxs-lookup"><span data-stu-id="8948c-104">D3DX\_R8G8B8A8\_UINT\_to\_UINT4 function</span></span>

<span data-ttu-id="8948c-105">Décompresse les \_ \_ \_ données de nuanceur dxgi R8G8B8A8 uint dans un XMUINT4.</span><span class="sxs-lookup"><span data-stu-id="8948c-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_UINT shader data to an XMUINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="8948c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8948c-106">Syntax</span></span>

``` syntax
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="8948c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8948c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8948c-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="8948c-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8948c-109">Données de nuanceur compressées.</span><span class="sxs-lookup"><span data-stu-id="8948c-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8948c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8948c-110">Return value</span></span>

<span data-ttu-id="8948c-111">Données de nuanceur décompressées.</span><span class="sxs-lookup"><span data-stu-id="8948c-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="8948c-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8948c-112">Requirements</span></span>



| <span data-ttu-id="8948c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8948c-113">Requirement</span></span> | <span data-ttu-id="8948c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8948c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8948c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="8948c-115">Header</span></span><br/> | <dl> <span data-ttu-id="8948c-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="8948c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8948c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8948c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8948c-118">Fonctions</span><span class="sxs-lookup"><span data-stu-id="8948c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="8948c-119">Décompresser et compresser le \_ format DXGI pour la modification des images In-Place</span><span class="sxs-lookup"><span data-stu-id="8948c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





