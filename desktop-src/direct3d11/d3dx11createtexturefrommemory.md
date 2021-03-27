---
title: D3DX11CreateTextureFromMemory, fonction (D3DX11. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser ces bibliothèques DirectXTK (Runtime), CreateXXXTextureFromMemory (où XXX est DDS ou WIC) DirectXTex Library (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA en tant que format de source d’art courant pour les jeux), puis CreateTexture créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.'
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- Fonction D3DX11CreateTextureFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953930"
---
# <a name="d3dx11createtexturefrommemory-function"></a><span data-ttu-id="1502b-105">D3DX11CreateTextureFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="1502b-105">D3DX11CreateTextureFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="1502b-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="1502b-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="1502b-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="1502b-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="1502b-108">Bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) (Runtime), **CREATEXXXTEXTUREFROMMEMORY** (où xxx est DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="1502b-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="1502b-109">Bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux, puis **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="1502b-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="1502b-110">Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="1502b-110">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1502b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1502b-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="1502b-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1502b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1502b-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1502b-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-114">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="1502b-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="1502b-115">Pointeur vers l’appareil (consultez [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="1502b-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1502b-116">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1502b-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-117">Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1502b-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1502b-118">Pointeur vers la ressource dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="1502b-118">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="1502b-119">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1502b-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-120">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1502b-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1502b-121">Taille de la ressource dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="1502b-121">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="1502b-122">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1502b-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-123">Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1502b-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="1502b-124">facultatif.</span><span class="sxs-lookup"><span data-stu-id="1502b-124">Optional.</span></span> <span data-ttu-id="1502b-125">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="1502b-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1502b-126">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1502b-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-127">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1502b-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="1502b-128">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1502b-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="1502b-129">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="1502b-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="1502b-130">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1502b-130">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-131">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="1502b-131">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="1502b-132">Adresse d’un pointeur vers la ressource créée.</span><span class="sxs-lookup"><span data-stu-id="1502b-132">Address of a pointer to the created resource.</span></span> <span data-ttu-id="1502b-133">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="1502b-133">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="1502b-134">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1502b-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1502b-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1502b-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1502b-136">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1502b-136">A pointer to the return value.</span></span> <span data-ttu-id="1502b-137">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1502b-137">May be **NULL**.</span></span> <span data-ttu-id="1502b-138">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="1502b-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1502b-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1502b-139">Return value</span></span>

<span data-ttu-id="1502b-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1502b-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1502b-141">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1502b-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1502b-142">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1502b-142">Requirements</span></span>



| <span data-ttu-id="1502b-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1502b-143">Requirement</span></span> | <span data-ttu-id="1502b-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1502b-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1502b-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="1502b-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1502b-146"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="1502b-146"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="1502b-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1502b-147">Library</span></span><br/> | <dl> <span data-ttu-id="1502b-148"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1502b-148"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1502b-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1502b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1502b-150">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="1502b-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

