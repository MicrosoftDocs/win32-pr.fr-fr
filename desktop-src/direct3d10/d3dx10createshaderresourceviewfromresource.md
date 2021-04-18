---
description: Créer un affichage des ressources de nuanceur à partir d’une ressource.
ms.assetid: 207cda5f-5b7e-420a-988f-135cd2a04eb0
title: D3DX10CreateShaderResourceViewFromResource, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 12de92153b6f812b4f014f53e918e7a97000eda6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520329"
---
# <a name="d3dx10createshaderresourceviewfromresource-function"></a><span data-ttu-id="752b1-103">D3DX10CreateShaderResourceViewFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="752b1-103">D3DX10CreateShaderResourceViewFromResource function</span></span>

<span data-ttu-id="752b1-104">Créer un affichage des ressources de nuanceur à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="752b1-104">Create a shader-resource view from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="752b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="752b1-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromResource(
  _In_  ID3D10Device             *pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="752b1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="752b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="752b1-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752b1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="752b1-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="752b1-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="752b1-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="752b1-110">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752b1-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-111">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="752b1-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="752b1-112">Handle du module de ressources contenant l’affichage des ressources du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="752b1-112">Handle to the resource module containing the shader-resource view.</span></span> <span data-ttu-id="752b1-113">HMODULE peut être obtenu avec la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="752b1-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="752b1-114">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752b1-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-115">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="752b1-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="752b1-116">Nom de l’affichage des ressources de nuanceur dans hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="752b1-116">Name of the shader resource view in hSrcModule.</span></span> <span data-ttu-id="752b1-117">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="752b1-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="752b1-118">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="752b1-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="752b1-119">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752b1-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-120">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="752b1-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="752b1-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="752b1-121">Optional.</span></span> <span data-ttu-id="752b1-122">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="752b1-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="752b1-123">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="752b1-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-124">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="752b1-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="752b1-125">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="752b1-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="752b1-126">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="752b1-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="752b1-127">*ppShaderResourceView* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="752b1-127">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-128">Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="752b1-128">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="752b1-129">Adresse d’un pointeur vers l’affichage des ressources du nuanceur (voir [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="752b1-129">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="752b1-130">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="752b1-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="752b1-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="752b1-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="752b1-132">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="752b1-132">A pointer to the return value.</span></span> <span data-ttu-id="752b1-133">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="752b1-133">May be **NULL**.</span></span> <span data-ttu-id="752b1-134">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="752b1-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="752b1-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="752b1-135">Return value</span></span>

<span data-ttu-id="752b1-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="752b1-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="752b1-137">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="752b1-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="752b1-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="752b1-138">Requirements</span></span>



| <span data-ttu-id="752b1-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="752b1-139">Requirement</span></span> | <span data-ttu-id="752b1-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="752b1-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="752b1-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="752b1-141">Header</span></span><br/>  | <dl> <span data-ttu-id="752b1-142"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="752b1-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="752b1-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="752b1-143">Library</span></span><br/> | <dl> <span data-ttu-id="752b1-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="752b1-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="752b1-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="752b1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752b1-146">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="752b1-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="752b1-147">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="752b1-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
