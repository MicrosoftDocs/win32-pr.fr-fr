---
description: Charge une texture à partir d’une texture.
ms.assetid: 126e71e1-a3b2-418b-be35-434a2e9472ca
title: D3DX10LoadTextureFromTexture, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10LoadTextureFromTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e8dc65c9bff78484f09c355f8eb3d9626372b9b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322750"
---
# <a name="d3dx10loadtexturefromtexture-function"></a><span data-ttu-id="35df3-103">D3DX10LoadTextureFromTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="35df3-103">D3DX10LoadTextureFromTexture function</span></span>

<span data-ttu-id="35df3-104">Charge une texture à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="35df3-104">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="35df3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35df3-105">Syntax</span></span>


```C++
HRESULT D3DX10LoadTextureFromTexture(
   ID3D10Resource           *pSrcTexture,
   D3DX10_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D10Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="35df3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35df3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35df3-107">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="35df3-107">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="35df3-108">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="35df3-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="35df3-109">Pointeur vers la texture source.</span><span class="sxs-lookup"><span data-stu-id="35df3-109">Pointer to the source texture.</span></span> <span data-ttu-id="35df3-110">Consultez [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="35df3-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="35df3-111">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="35df3-111">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="35df3-112">Type : **[ **d3dx10 \_ texture \_ load \_ info**](d3dx10-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="35df3-112">Type: **[**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md)\***</span></span>

<span data-ttu-id="35df3-113">Pointeur vers les paramètres de chargement de texture.</span><span class="sxs-lookup"><span data-stu-id="35df3-113">Pointer to texture loading parameters.</span></span> <span data-ttu-id="35df3-114">Consultez [**d3dx10 \_ texture \_ load \_ info**](d3dx10-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="35df3-114">See [**D3DX10\_TEXTURE\_LOAD\_INFO**](d3dx10-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="35df3-115">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="35df3-115">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="35df3-116">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="35df3-116">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="35df3-117">Pointeur vers la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="35df3-117">Pointer to the destination texture.</span></span> <span data-ttu-id="35df3-118">Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="35df3-118">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35df3-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35df3-119">Return value</span></span>

<span data-ttu-id="35df3-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35df3-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35df3-121">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="35df3-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35df3-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35df3-122">Requirements</span></span>



| <span data-ttu-id="35df3-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35df3-123">Requirement</span></span> | <span data-ttu-id="35df3-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="35df3-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35df3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="35df3-125">Header</span></span><br/> | <dl> <span data-ttu-id="35df3-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="35df3-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35df3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35df3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35df3-128">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="35df3-128">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




