---
title: D3DX11LoadTextureFromTexture, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, redimensionner, convertir, compresser, décompresser et/ou CopyRectangle. Charge une texture à partir d’une texture.'
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- Fonction D3DX11LoadTextureFromTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974591"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="3bf8f-106">D3DX11LoadTextureFromTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="3bf8f-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="3bf8f-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="3bf8f-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **Redimensionner**, **convertir**, **compresser**, **décompresser** et/ou **CopyRectangle**.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="3bf8f-109">Charge une texture à partir d’une texture.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf8f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bf8f-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="3bf8f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bf8f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf8f-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="3bf8f-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf8f-113">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="3bf8f-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="3bf8f-114">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="3bf8f-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="3bf8f-115">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="3bf8f-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf8f-116">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="3bf8f-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="3bf8f-117">Pointeur vers la texture source.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-117">Pointer to the source texture.</span></span> <span data-ttu-id="3bf8f-118">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="3bf8f-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="3bf8f-119">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="3bf8f-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf8f-120">Type : **[ **D3DX11 \_ texture \_ load \_ info**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bf8f-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="3bf8f-121">Pointeur vers les paramètres de chargement de texture.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="3bf8f-122">Consultez [**D3DX11 \_ texture \_ load \_ info**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="3bf8f-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bf8f-123">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="3bf8f-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="3bf8f-124">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="3bf8f-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="3bf8f-125">Pointeur vers la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-125">Pointer to the destination texture.</span></span> <span data-ttu-id="3bf8f-126">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="3bf8f-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf8f-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bf8f-127">Return value</span></span>

<span data-ttu-id="3bf8f-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bf8f-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bf8f-129">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3bf8f-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf8f-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3bf8f-130">Requirements</span></span>



| <span data-ttu-id="3bf8f-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bf8f-131">Requirement</span></span> | <span data-ttu-id="3bf8f-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bf8f-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf8f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bf8f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3bf8f-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bf8f-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3bf8f-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3bf8f-135">Library</span></span><br/> | <dl> <span data-ttu-id="3bf8f-136"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bf8f-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3bf8f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bf8f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bf8f-138">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="3bf8f-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





