---
title: D3D12IsLayoutOpaque, fonction (D3dx12. h)
description: Indique si la disposition est opaque.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque fonction)
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531314"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="2429f-104">D3D12IsLayoutOpaque fonction)</span><span class="sxs-lookup"><span data-stu-id="2429f-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="2429f-105">Indique si la disposition est opaque.</span><span class="sxs-lookup"><span data-stu-id="2429f-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="2429f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2429f-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="2429f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2429f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2429f-108">*Disposition*</span><span class="sxs-lookup"><span data-stu-id="2429f-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="2429f-109">Type : **[ **\_ \_ mise en page de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="2429f-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="2429f-110">Disposition à vérifier, en tant que [**\_ \_ disposition de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="2429f-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2429f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2429f-111">Return value</span></span>

<span data-ttu-id="2429f-112">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="2429f-112">Type: **bool**</span></span>

<span data-ttu-id="2429f-113">Valeur **booléenne** qui indique si la disposition est opaque.</span><span class="sxs-lookup"><span data-stu-id="2429f-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="2429f-114">Une disposition est opaque si elle est D3D12 \_ disposition de texture \_ \_ inconnue ou \_ disposition de texture D3D12 \_ \_ 64 Ko \_ non définis \_ SWIZZLE.</span><span class="sxs-lookup"><span data-stu-id="2429f-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2429f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2429f-115">Requirements</span></span>



| <span data-ttu-id="2429f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2429f-116">Requirement</span></span> | <span data-ttu-id="2429f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2429f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2429f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="2429f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2429f-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2429f-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="2429f-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2429f-120">Library</span></span><br/> | <dl> <span data-ttu-id="2429f-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2429f-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="2429f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2429f-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2429f-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2429f-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2429f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2429f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2429f-125">Fonctions d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="2429f-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





