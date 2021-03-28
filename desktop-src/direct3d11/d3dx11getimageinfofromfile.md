---
title: D3DX11GetImageInfoFromFile, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, GetMetadataFromXXXFile (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Récupère des informations sur un fichier image donné.'
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Fonction D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043146"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="6f050-106">D3DX11GetImageInfoFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="6f050-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="6f050-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6f050-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="6f050-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXFILE** (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="6f050-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="6f050-109">Récupère des informations sur un fichier image donné.</span><span class="sxs-lookup"><span data-stu-id="6f050-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f050-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f050-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="6f050-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f050-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f050-112">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f050-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f050-113">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6f050-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6f050-114">Nom de fichier de l’image sur laquelle récupérer des informations.</span><span class="sxs-lookup"><span data-stu-id="6f050-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="6f050-115">Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="6f050-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="6f050-116">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f050-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f050-117">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f050-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="6f050-118">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6f050-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="6f050-119">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6f050-119">Can be **NULL**.</span></span> <span data-ttu-id="6f050-120">Voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="6f050-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f050-121">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f050-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f050-122">Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f050-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="6f050-123">Pointeur vers les [**\_ \_ informations d’image D3DX11**](d3dx11-image-info.md) à remplir avec la description des données dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="6f050-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="6f050-124">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6f050-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f050-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="6f050-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="6f050-126">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6f050-126">A pointer to the return value.</span></span> <span data-ttu-id="6f050-127">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6f050-127">May be **NULL**.</span></span> <span data-ttu-id="6f050-128">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="6f050-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f050-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f050-129">Return value</span></span>

<span data-ttu-id="6f050-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f050-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f050-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f050-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6f050-132">Si la fonction échoue, la valeur de retour peut être la suivante : D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="6f050-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="6f050-133">Notes</span><span class="sxs-lookup"><span data-stu-id="6f050-133">Remarks</span></span>

<span data-ttu-id="6f050-134">Cette fonction prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="6f050-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f050-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f050-135">Requirements</span></span>



| <span data-ttu-id="6f050-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f050-136">Requirement</span></span> | <span data-ttu-id="6f050-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f050-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f050-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f050-138">Header</span></span><br/>  | <dl> <span data-ttu-id="6f050-139"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f050-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6f050-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f050-140">Library</span></span><br/> | <dl> <span data-ttu-id="6f050-141"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f050-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6f050-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f050-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f050-143">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="6f050-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

