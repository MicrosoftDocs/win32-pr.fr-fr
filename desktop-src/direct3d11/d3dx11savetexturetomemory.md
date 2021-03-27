---
title: D3DX11SaveTextureToMemory, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, CaptureTexture Then SaveToXXXMemory (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Enregistrer une texture dans la mémoire.'
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- Fonction D3DX11SaveTextureToMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211874"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="73fc8-106">D3DX11SaveTextureToMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="73fc8-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="73fc8-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="73fc8-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="73fc8-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** Then **SAVETOXXXMEMORY** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="73fc8-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="73fc8-109">Enregistrer une texture dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="73fc8-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fc8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73fc8-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="73fc8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73fc8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73fc8-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="73fc8-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="73fc8-113">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="73fc8-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="73fc8-114">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="73fc8-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="73fc8-115">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73fc8-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fc8-116">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="73fc8-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="73fc8-117">Pointeur vers la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="73fc8-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="73fc8-118">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="73fc8-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="73fc8-119">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73fc8-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fc8-120">Type : **[ **D3DX11 \_ image \_ file \_ format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="73fc8-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="73fc8-121">Format dans lequel la texture sera enregistrée.</span><span class="sxs-lookup"><span data-stu-id="73fc8-121">The format the texture will be saved as.</span></span> <span data-ttu-id="73fc8-122">Consultez [**\_ format de \_ fichier \_ image D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="73fc8-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="73fc8-123">*ppDestBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73fc8-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73fc8-124">Type : **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="73fc8-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="73fc8-125">Adresse d’un pointeur vers la mémoire contenant la texture enregistrée.</span><span class="sxs-lookup"><span data-stu-id="73fc8-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="73fc8-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="73fc8-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73fc8-127">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="73fc8-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="73fc8-128">facultatif.</span><span class="sxs-lookup"><span data-stu-id="73fc8-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73fc8-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73fc8-129">Return value</span></span>

<span data-ttu-id="73fc8-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="73fc8-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="73fc8-131">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="73fc8-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73fc8-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="73fc8-132">Requirements</span></span>



| <span data-ttu-id="73fc8-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73fc8-133">Requirement</span></span> | <span data-ttu-id="73fc8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="73fc8-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73fc8-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="73fc8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="73fc8-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="73fc8-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="73fc8-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="73fc8-137">Library</span></span><br/> | <dl> <span data-ttu-id="73fc8-138"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73fc8-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="73fc8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73fc8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fc8-140">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="73fc8-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

