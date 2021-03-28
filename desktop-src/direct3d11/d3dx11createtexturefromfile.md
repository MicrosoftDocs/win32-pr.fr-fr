---
title: D3DX11CreateTextureFromFile, fonction (D3DX11. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser ces bibliothèques DirectXTK (Runtime), CreateXXXTextureFromFile (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXFile (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA en tant que format de source d’art courant pour les jeux), puis CreateTexture créer une ressource de texture à partir d’un fichier.'
ms.assetid: a84ea166-2296-48d9-a028-b65fd68f2371
keywords:
- Fonction D3DX11CreateTextureFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ab9bedcfe44238938e47ccb402738d2694b061
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992273"
---
# <a name="d3dx11createtexturefromfile-function"></a><span data-ttu-id="e9f2d-105">D3DX11CreateTextureFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="e9f2d-105">D3DX11CreateTextureFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="e9f2d-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e9f2d-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e9f2d-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="e9f2d-108">Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMFILE** (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="e9f2d-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="e9f2d-109">Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXFILE** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="e9f2d-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="e9f2d-110">Créer une ressource de texture à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-110">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f2d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9f2d-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromFile(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e9f2d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9f2d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f2d-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-114">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="e9f2d-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="e9f2d-115">Pointeur vers l’appareil (consultez [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2d-116">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e9f2d-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e9f2d-118">Nom du fichier contenant la ressource.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-118">The name of the file containing the resource.</span></span> <span data-ttu-id="e9f2d-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e9f2d-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2d-121">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-122">Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9f2d-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="e9f2d-123">facultatif.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-123">Optional.</span></span> <span data-ttu-id="e9f2d-124">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2d-125">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-126">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e9f2d-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="e9f2d-127">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-127">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="e9f2d-128">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2d-129">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-129">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-130">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="e9f2d-130">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="e9f2d-131">Adresse d’un pointeur vers la ressource de texture (consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-131">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="e9f2d-132">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9f2d-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2d-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e9f2d-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e9f2d-134">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-134">A pointer to the return value.</span></span> <span data-ttu-id="e9f2d-135">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-135">May be **NULL**.</span></span> <span data-ttu-id="e9f2d-136">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="e9f2d-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f2d-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9f2d-137">Return value</span></span>

<span data-ttu-id="e9f2d-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9f2d-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9f2d-139">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="e9f2d-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f2d-140">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e9f2d-140">Requirements</span></span>



| <span data-ttu-id="e9f2d-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f2d-141">Requirement</span></span> | <span data-ttu-id="e9f2d-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f2d-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f2d-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f2d-143">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f2d-144"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f2d-144"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9f2d-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e9f2d-145">Library</span></span><br/> | <dl> <span data-ttu-id="e9f2d-146"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9f2d-146"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f2d-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f2d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f2d-148">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="e9f2d-148">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

