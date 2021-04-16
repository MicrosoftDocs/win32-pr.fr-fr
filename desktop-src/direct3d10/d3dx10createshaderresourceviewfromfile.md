---
description: Créer un affichage des ressources de nuanceur à partir d’un fichier.
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: D3DX10CreateShaderResourceViewFromFile, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394160"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="5a954-103">D3DX10CreateShaderResourceViewFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="5a954-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="5a954-104">Créer un affichage des ressources de nuanceur à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="5a954-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a954-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a954-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="5a954-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a954-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a954-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a954-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="5a954-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="5a954-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="5a954-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5a954-110">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a954-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-111">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a954-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a954-112">Nom du fichier qui contient l’affichage des ressources du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="5a954-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="5a954-113">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5a954-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5a954-114">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5a954-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5a954-115">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a954-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-116">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a954-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="5a954-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5a954-117">Optional.</span></span> <span data-ttu-id="5a954-118">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="5a954-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5a954-119">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a954-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-120">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a954-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="5a954-121">Pointeur vers une interface thread-Pump (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5a954-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="5a954-122">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="5a954-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="5a954-123">*ppShaderResourceView* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a954-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-124">Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="5a954-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="5a954-125">Adresse d’un pointeur vers l’affichage des ressources du nuanceur (voir [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="5a954-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="5a954-126">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a954-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a954-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5a954-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5a954-128">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5a954-128">A pointer to the return value.</span></span> <span data-ttu-id="5a954-129">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5a954-129">May be **NULL**.</span></span> <span data-ttu-id="5a954-130">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="5a954-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a954-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a954-131">Return value</span></span>

<span data-ttu-id="5a954-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a954-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a954-133">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5a954-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a954-134">Notes</span><span class="sxs-lookup"><span data-stu-id="5a954-134">Remarks</span></span>

<span data-ttu-id="5a954-135">Pour obtenir la liste des formats d’image pris en charge, consultez [**\_ \_ \_ format de fichier image d3dx10**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="5a954-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a954-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a954-136">Requirements</span></span>



| <span data-ttu-id="5a954-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a954-137">Requirement</span></span> | <span data-ttu-id="5a954-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a954-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a954-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a954-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5a954-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a954-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5a954-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a954-141">Library</span></span><br/> | <dl> <span data-ttu-id="5a954-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a954-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5a954-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a954-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a954-144">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="5a954-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="5a954-145">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="5a954-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
