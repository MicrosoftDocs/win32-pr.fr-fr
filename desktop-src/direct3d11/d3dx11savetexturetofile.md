---
title: D3DX11SaveTextureToFile, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, CaptureTexture Then SaveToXXXFile (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque DirectXTK, SaveDDSTextureToFile ou SaveWICTextureToFile. Enregistrer une texture dans un fichier.'
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- Fonction D3DX11SaveTextureToFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974587"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="8023f-107">D3DX11SaveTextureToFile fonction)</span><span class="sxs-lookup"><span data-stu-id="8023f-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="8023f-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="8023f-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="8023f-109">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **CaptureTexture** Then **SAVETOXXXFILE** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="8023f-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="8023f-110">Pour le scénario simplifié de création d’une capture d’écran à partir d’une texture de cible de rendu, nous vous recommandons d’utiliser la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SaveDDSTextureToFile** ou **SaveWICTextureToFile**.</span><span class="sxs-lookup"><span data-stu-id="8023f-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="8023f-111">Enregistrer une texture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="8023f-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8023f-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8023f-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="8023f-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8023f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8023f-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="8023f-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="8023f-115">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="8023f-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="8023f-116">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="8023f-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="8023f-117">*pSrcTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8023f-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8023f-118">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="8023f-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="8023f-119">Pointeur vers la texture à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="8023f-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="8023f-120">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="8023f-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="8023f-121">*DestFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8023f-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8023f-122">Type : **[ **D3DX11 \_ image \_ file \_ format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="8023f-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="8023f-123">Format dans lequel la texture sera enregistrée (voir [**format de \_ \_ fichier image \_ D3DX11**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="8023f-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="8023f-124">D3DX11 \_ IFF \_ DDS est le format par défaut, car il s’agit de la seule option qui prend en charge tous les formats au [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="8023f-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="8023f-125">*pDestFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8023f-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8023f-126">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8023f-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8023f-127">Nom du fichier de sortie de destination dans lequel la texture sera enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8023f-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="8023f-128">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8023f-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8023f-129">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8023f-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8023f-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8023f-130">Return value</span></span>

<span data-ttu-id="8023f-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8023f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8023f-132">La valeur de retour est l’une des valeurs énumérées dans les [codes de retour de Direct3D 11](d3d11-graphics-reference-returnvalues.md). Utilisez la valeur de retour pour voir si le *DestFormat* est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8023f-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="8023f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="8023f-133">Remarks</span></span>

<span data-ttu-id="8023f-134">**D3DX11SaveTextureToFile** écrit la structure [**\_ \_ DXT10 en-tête DDS**](/windows/desktop/direct3ddds/dds-header-dxt10) supplémentaire pour la texture d’entrée uniquement si nécessaire (par exemple, parce que la texture d’entrée est au format RVB standard (sRVB)).</span><span class="sxs-lookup"><span data-stu-id="8023f-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="8023f-135">Si **D3DX11SaveTextureToFile** écrit la structure **DXT10 de l' \_ en-tête \_ DDS** , il définit le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) pour la texture sur **facilement** pour indiquer le Prescense de l’en-tête étendu DXT10 de l' **\_ en-tête \_ DDS** .</span><span class="sxs-lookup"><span data-stu-id="8023f-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="8023f-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8023f-136">Requirements</span></span>



| <span data-ttu-id="8023f-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8023f-137">Requirement</span></span> | <span data-ttu-id="8023f-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="8023f-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8023f-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="8023f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8023f-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8023f-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8023f-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8023f-141">Library</span></span><br/> | <dl> <span data-ttu-id="8023f-142"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8023f-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8023f-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8023f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8023f-144">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="8023f-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

