---
description: Créer une texture à partir d’une autre ressource.
ms.assetid: 9758968a-652f-42bb-8c81-ad7816c57b17
title: D3DX10CreateTextureFromResource, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 22be3b54c7aa9090fd95624a51bc248b01003dcc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524875"
---
# <a name="d3dx10createtexturefromresource-function"></a><span data-ttu-id="f078a-103">D3DX10CreateTextureFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="f078a-103">D3DX10CreateTextureFromResource function</span></span>

<span data-ttu-id="f078a-104">Créer une texture à partir d’une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="f078a-104">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="f078a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f078a-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromResource(
  _In_  ID3D10Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="f078a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f078a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f078a-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f078a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="f078a-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="f078a-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="f078a-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f078a-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f078a-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f078a-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f078a-112">Handle de la ressource source.</span><span class="sxs-lookup"><span data-stu-id="f078a-112">A handle to the source resource.</span></span> <span data-ttu-id="f078a-113">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="f078a-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="f078a-114">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f078a-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f078a-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f078a-116">Chaîne qui contient le nom de la ressource source.</span><span class="sxs-lookup"><span data-stu-id="f078a-116">A string that contains the name of the source resource.</span></span> <span data-ttu-id="f078a-117">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f078a-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f078a-118">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f078a-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f078a-119">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f078a-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-120">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f078a-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="f078a-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f078a-121">Optional.</span></span> <span data-ttu-id="f078a-122">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="f078a-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f078a-123">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f078a-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-124">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="f078a-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="f078a-125">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="f078a-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="f078a-126">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="f078a-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="f078a-127">*ppTexture* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f078a-127">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-128">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="f078a-128">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="f078a-129">Adresse d’un pointeur vers la ressource de texture (consultez [**ID3D10Resource interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span><span class="sxs-lookup"><span data-stu-id="f078a-129">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="f078a-130">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f078a-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f078a-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="f078a-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="f078a-132">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f078a-132">A pointer to the return value.</span></span> <span data-ttu-id="f078a-133">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f078a-133">May be **NULL**.</span></span> <span data-ttu-id="f078a-134">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="f078a-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f078a-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f078a-135">Return value</span></span>

<span data-ttu-id="f078a-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f078a-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f078a-137">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f078a-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f078a-138">Notes</span><span class="sxs-lookup"><span data-stu-id="f078a-138">Remarks</span></span>

<span data-ttu-id="f078a-139">Pour obtenir la liste des formats d’image pris en charge, consultez [**d3dx10 \_ image \_ file \_ format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="f078a-139">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f078a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f078a-140">Requirements</span></span>



| <span data-ttu-id="f078a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f078a-141">Requirement</span></span> | <span data-ttu-id="f078a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f078a-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f078a-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="f078a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="f078a-144"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f078a-144"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f078a-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f078a-145">Library</span></span><br/> | <dl> <span data-ttu-id="f078a-146"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f078a-146"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f078a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f078a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f078a-148">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="f078a-148">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="f078a-149">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="f078a-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
