---
description: Créer une ressource de texture à partir d’un fichier.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: D3DX10CreateTextureFromFile, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535822"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="14164-103">D3DX10CreateTextureFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="14164-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="14164-104">Créer une ressource de texture à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="14164-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="14164-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14164-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="14164-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14164-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14164-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="14164-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="14164-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="14164-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="14164-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14164-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14164-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14164-112">Nom du fichier contenant la ressource.</span><span class="sxs-lookup"><span data-stu-id="14164-112">The name of the file containing the resource.</span></span> <span data-ttu-id="14164-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="14164-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="14164-114">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="14164-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="14164-115">Pour obtenir la liste des formats de fichier image pris en charge, consultez énumération de [**\_ \_ \_ format de fichier image d3dx10**](d3dx10-image-file-format.md) .</span><span class="sxs-lookup"><span data-stu-id="14164-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="14164-116">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14164-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-117">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="14164-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="14164-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="14164-118">Optional.</span></span> <span data-ttu-id="14164-119">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="14164-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="14164-120">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14164-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-121">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="14164-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="14164-122">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="14164-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="14164-123">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="14164-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="14164-124">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14164-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-125">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="14164-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="14164-126">Adresse d’un pointeur vers la ressource de texture (consultez [**ID3D10Resource interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="14164-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="14164-127">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14164-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14164-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="14164-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="14164-129">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="14164-129">A pointer to the return value.</span></span> <span data-ttu-id="14164-130">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="14164-130">May be **NULL**.</span></span> <span data-ttu-id="14164-131">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="14164-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14164-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14164-132">Return value</span></span>

<span data-ttu-id="14164-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14164-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14164-134">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="14164-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="14164-135">Notes</span><span class="sxs-lookup"><span data-stu-id="14164-135">Remarks</span></span>

<span data-ttu-id="14164-136">Pour obtenir la liste des formats d’image pris en charge, consultez [**d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="14164-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14164-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14164-137">Requirements</span></span>



| <span data-ttu-id="14164-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14164-138">Requirement</span></span> | <span data-ttu-id="14164-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="14164-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14164-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="14164-140">Header</span></span><br/>  | <dl> <span data-ttu-id="14164-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="14164-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="14164-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14164-142">Library</span></span><br/> | <dl> <span data-ttu-id="14164-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14164-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14164-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14164-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14164-145">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="14164-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="14164-146">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="14164-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
