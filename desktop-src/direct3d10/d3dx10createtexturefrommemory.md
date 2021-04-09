---
description: Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: D3DX10CreateTextureFromMemory, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953826"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="be77d-103">D3DX10CreateTextureFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="be77d-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="be77d-104">Créer une ressource de texture à partir d’un fichier résidant dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="be77d-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="be77d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be77d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="be77d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be77d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be77d-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be77d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="be77d-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="be77d-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="be77d-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="be77d-110">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be77d-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-111">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be77d-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be77d-112">Pointeur vers la ressource dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="be77d-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="be77d-113">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be77d-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-114">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be77d-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be77d-115">Taille de la ressource dans la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="be77d-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="be77d-116">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be77d-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-117">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="be77d-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="be77d-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="be77d-118">Optional.</span></span> <span data-ttu-id="be77d-119">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="be77d-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="be77d-120">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be77d-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-121">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="be77d-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="be77d-122">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="be77d-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="be77d-123">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="be77d-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="be77d-124">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be77d-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-125">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="be77d-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="be77d-126">Adresse d’un pointeur vers la ressource créée.</span><span class="sxs-lookup"><span data-stu-id="be77d-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="be77d-127">Voir [**interface ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="be77d-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="be77d-128">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="be77d-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be77d-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="be77d-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="be77d-130">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="be77d-130">A pointer to the return value.</span></span> <span data-ttu-id="be77d-131">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="be77d-131">May be **NULL**.</span></span> <span data-ttu-id="be77d-132">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="be77d-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be77d-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be77d-133">Return value</span></span>

<span data-ttu-id="be77d-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be77d-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be77d-135">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="be77d-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="be77d-136">Notes</span><span class="sxs-lookup"><span data-stu-id="be77d-136">Remarks</span></span>

<span data-ttu-id="be77d-137">Pour obtenir la liste des formats d’image pris en charge, consultez [**d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="be77d-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be77d-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be77d-138">Requirements</span></span>



| <span data-ttu-id="be77d-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be77d-139">Requirement</span></span> | <span data-ttu-id="be77d-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="be77d-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be77d-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="be77d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="be77d-142"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="be77d-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="be77d-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be77d-143">Library</span></span><br/> | <dl> <span data-ttu-id="be77d-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be77d-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be77d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be77d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be77d-146">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="be77d-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="be77d-147">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="be77d-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
