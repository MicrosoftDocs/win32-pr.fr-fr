---
title: D3DX11CreateTextureFromResource, fonction (D3DX11. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les fonctions de ressource, puis la bibliothèque DirectXTK (Runtime), CreateXXXTextureFromMemory (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis CreateTexture créera une texture à partir d’une autre ressource.'
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- Fonction D3DX11CreateTextureFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bea89fe4f8bf6632ada9461b048195335c72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211876"
---
# <a name="d3dx11createtexturefromresource-function"></a><span data-ttu-id="55d04-105">D3DX11CreateTextureFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="55d04-105">D3DX11CreateTextureFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="55d04-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="55d04-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="55d04-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les [fonctions de ressource](/windows/desktop/menurc/resources-functions), puis les suivantes :</span><span class="sxs-lookup"><span data-stu-id="55d04-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="55d04-108">Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="55d04-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="55d04-109">Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="55d04-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="55d04-110">Créer une texture à partir d’une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="55d04-110">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="55d04-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55d04-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="55d04-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55d04-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d04-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d04-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-114">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="55d04-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="55d04-115">Pointeur vers l’appareil (consultez [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="55d04-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="55d04-116">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d04-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-117">Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55d04-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="55d04-118">Handle de la ressource source.</span><span class="sxs-lookup"><span data-stu-id="55d04-118">A handle to the source resource.</span></span> <span data-ttu-id="55d04-119">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="55d04-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="55d04-120">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d04-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-121">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="55d04-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="55d04-122">Chaîne qui contient le nom de la ressource source.</span><span class="sxs-lookup"><span data-stu-id="55d04-122">A string that contains the name of the source resource.</span></span> <span data-ttu-id="55d04-123">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="55d04-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="55d04-124">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="55d04-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="55d04-125">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d04-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-126">Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="55d04-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="55d04-127">facultatif.</span><span class="sxs-lookup"><span data-stu-id="55d04-127">Optional.</span></span> <span data-ttu-id="55d04-128">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="55d04-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="55d04-129">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d04-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-130">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="55d04-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="55d04-131">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="55d04-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="55d04-132">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="55d04-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="55d04-133">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="55d04-133">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-134">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="55d04-134">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="55d04-135">Adresse d’un pointeur vers la ressource de texture (consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span><span class="sxs-lookup"><span data-stu-id="55d04-135">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="55d04-136">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="55d04-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55d04-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="55d04-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="55d04-138">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="55d04-138">A pointer to the return value.</span></span> <span data-ttu-id="55d04-139">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="55d04-139">May be **NULL**.</span></span> <span data-ttu-id="55d04-140">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="55d04-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d04-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55d04-141">Return value</span></span>

<span data-ttu-id="55d04-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="55d04-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="55d04-143">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="55d04-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55d04-144">Spécifications</span><span class="sxs-lookup"><span data-stu-id="55d04-144">Requirements</span></span>



| <span data-ttu-id="55d04-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55d04-145">Requirement</span></span> | <span data-ttu-id="55d04-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d04-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55d04-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="55d04-147">Header</span></span><br/>  | <dl> <span data-ttu-id="55d04-148"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d04-148"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="55d04-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55d04-149">Library</span></span><br/> | <dl> <span data-ttu-id="55d04-150"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55d04-150"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d04-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55d04-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d04-152">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="55d04-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

