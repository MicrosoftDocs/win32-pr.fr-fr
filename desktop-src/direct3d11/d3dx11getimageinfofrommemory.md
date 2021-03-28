---
title: D3DX11GetImageInfoFromMemory, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, GetMetadataFromXXXMemory (où XXX est WIC, DDS ou TGA ; WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux. Obtenir des informations sur une image déjà chargée en mémoire.'
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- Fonction D3DX11GetImageInfoFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974594"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="b9ec5-106">D3DX11GetImageInfoFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="b9ec5-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="b9ec5-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9ec5-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GETMETADATAFROMXXXMEMORY** (où xxx est WIC, DDS ou TGA. WIC ne prend pas en charge DDS et TGA. D3DX 9 prenait en charge la TGA comme format de source d’art courant pour les jeux.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="b9ec5-109">Obtenir des informations sur une image déjà chargée en mémoire.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ec5-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9ec5-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b9ec5-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9ec5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ec5-112">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9ec5-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ec5-113">Type : **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9ec5-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b9ec5-114">Pointeur vers l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b9ec5-115">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9ec5-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ec5-116">Type : **[ **taille \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b9ec5-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b9ec5-117">Taille de l’image en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b9ec5-118">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9ec5-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ec5-119">Type : **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9ec5-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="b9ec5-120">Pompe de thread facultative qui peut être utilisée pour charger les informations de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="b9ec5-121">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-121">Can be **NULL**.</span></span> <span data-ttu-id="b9ec5-122">Voir [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b9ec5-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9ec5-123">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9ec5-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ec5-124">Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b9ec5-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="b9ec5-125">Informations sur l’image en mémoire.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="b9ec5-126">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b9ec5-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ec5-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b9ec5-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b9ec5-128">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-128">A pointer to the return value.</span></span> <span data-ttu-id="b9ec5-129">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-129">May be **NULL**.</span></span> <span data-ttu-id="b9ec5-130">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="b9ec5-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ec5-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9ec5-131">Return value</span></span>

<span data-ttu-id="b9ec5-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9ec5-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9ec5-133">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b9ec5-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ec5-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b9ec5-134">Requirements</span></span>



| <span data-ttu-id="b9ec5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9ec5-135">Requirement</span></span> | <span data-ttu-id="b9ec5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9ec5-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ec5-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9ec5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b9ec5-138"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ec5-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b9ec5-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9ec5-139">Library</span></span><br/> | <dl> <span data-ttu-id="b9ec5-140"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ec5-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b9ec5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9ec5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ec5-142">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="b9ec5-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

