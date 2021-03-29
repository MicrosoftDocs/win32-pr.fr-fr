---
title: D3DX11CreateShaderResourceViewFromFile, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser ces bibliothèques DirectXTK (Runtime), CreateXXXTextureFromFile (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXFile (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA en tant que format de source d’art courant pour les jeux), puis CreateShaderResourceView créer un affichage des ressources de nuanceur à partir d’un fichier.'
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- Fonction D3DX11CreateShaderResourceViewFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323117"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="28475-105">D3DX11CreateShaderResourceViewFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="28475-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="28475-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="28475-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="28475-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="28475-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="28475-108">Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="28475-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="28475-109">Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXFILE** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="28475-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="28475-110">Créer un affichage des ressources de nuanceur à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="28475-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="28475-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28475-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="28475-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28475-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28475-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28475-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-114">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="28475-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="28475-115">Pointeur vers l’appareil (consultez [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="28475-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="28475-116">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28475-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="28475-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="28475-118">Nom du fichier qui contient l’affichage des ressources du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="28475-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="28475-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="28475-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="28475-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="28475-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="28475-121">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28475-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-122">Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="28475-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="28475-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="28475-123">Optional.</span></span> <span data-ttu-id="28475-124">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="28475-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="28475-125">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28475-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-126">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="28475-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="28475-127">Pointeur vers une interface thread-Pump (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="28475-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="28475-128">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="28475-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="28475-129">*ppShaderResourceView* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28475-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-130">Type : **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="28475-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="28475-131">Adresse d’un pointeur vers l’affichage des ressources du nuanceur (voir [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="28475-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="28475-132">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28475-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28475-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="28475-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="28475-134">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="28475-134">A pointer to the return value.</span></span> <span data-ttu-id="28475-135">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="28475-135">May be **NULL**.</span></span> <span data-ttu-id="28475-136">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="28475-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28475-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28475-137">Return value</span></span>

<span data-ttu-id="28475-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28475-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28475-139">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="28475-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28475-140">Notes</span><span class="sxs-lookup"><span data-stu-id="28475-140">Remarks</span></span>

<span data-ttu-id="28475-141">Pour obtenir la liste des formats d’image pris en charge, consultez [**\_ \_ \_ format de fichier image D3DX11**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="28475-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28475-142">Spécifications</span><span class="sxs-lookup"><span data-stu-id="28475-142">Requirements</span></span>



| <span data-ttu-id="28475-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28475-143">Requirement</span></span> | <span data-ttu-id="28475-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="28475-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28475-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="28475-145">Header</span></span><br/>  | <dl> <span data-ttu-id="28475-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="28475-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="28475-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="28475-147">Library</span></span><br/> | <dl> <span data-ttu-id="28475-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28475-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="28475-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28475-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28475-150">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="28475-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

