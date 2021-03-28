---
title: D3DX11GetImageInfoFromResource, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les fonctions de ressource, puis d’utiliser la bibliothèque DirectXTex (outils), LoadFromXXXMemory (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Récupère des informations sur une image donnée dans une ressource.'
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- Fonction D3DX11GetImageInfoFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974595"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="25c1f-106">D3DX11GetImageInfoFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="25c1f-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="25c1f-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="25c1f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="25c1f-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser les [fonctions de ressource](/windows/desktop/menurc/resources-functions), puis d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) (outils), **LOADFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA). WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="25c1f-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="25c1f-109">Récupère des informations sur une image donnée dans une ressource.</span><span class="sxs-lookup"><span data-stu-id="25c1f-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c1f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25c1f-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="25c1f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25c1f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c1f-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25c1f-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c1f-113">Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25c1f-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25c1f-114">Module dans lequel la ressource est chargée.</span><span class="sxs-lookup"><span data-stu-id="25c1f-114">Module where the resource is loaded.</span></span> <span data-ttu-id="25c1f-115">Affectez la valeur **null** à ce paramètre pour spécifier le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="25c1f-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="25c1f-116">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25c1f-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c1f-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="25c1f-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="25c1f-118">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="25c1f-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="25c1f-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="25c1f-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="25c1f-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="25c1f-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="25c1f-121">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="25c1f-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="25c1f-122">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25c1f-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c1f-123">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="25c1f-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="25c1f-124">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="25c1f-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="25c1f-125">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="25c1f-125">Can be **NULL**.</span></span> <span data-ttu-id="25c1f-126">Voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="25c1f-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="25c1f-127">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25c1f-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c1f-128">Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="25c1f-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="25c1f-129">Pointeur vers une \_ structure d’informations d’image D3DX11 \_ à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="25c1f-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="25c1f-130">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25c1f-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25c1f-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="25c1f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="25c1f-132">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="25c1f-132">A pointer to the return value.</span></span> <span data-ttu-id="25c1f-133">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="25c1f-133">May be **NULL**.</span></span> <span data-ttu-id="25c1f-134">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="25c1f-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c1f-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25c1f-135">Return value</span></span>

<span data-ttu-id="25c1f-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25c1f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25c1f-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25c1f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="25c1f-138">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="25c1f-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="25c1f-139">Notes</span><span class="sxs-lookup"><span data-stu-id="25c1f-139">Remarks</span></span>

<span data-ttu-id="25c1f-140">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="25c1f-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="25c1f-141">Si Unicode est défini, l’appel de fonction est résolu en **D3DX11GetImageInfoFromResourceW**.</span><span class="sxs-lookup"><span data-stu-id="25c1f-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="25c1f-142">Dans le cas contraire, l’appel de fonction est résolu en **D3DX11GetImageInfoFromResourceA** , car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="25c1f-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c1f-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="25c1f-143">Requirements</span></span>



| <span data-ttu-id="25c1f-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25c1f-144">Requirement</span></span> | <span data-ttu-id="25c1f-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="25c1f-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25c1f-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="25c1f-146">Header</span></span><br/>  | <dl> <span data-ttu-id="25c1f-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c1f-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="25c1f-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25c1f-148">Library</span></span><br/> | <dl> <span data-ttu-id="25c1f-149"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25c1f-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="25c1f-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c1f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c1f-151">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="25c1f-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

