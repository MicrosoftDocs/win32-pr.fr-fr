---
description: Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.
ms.assetid: 8316987f-75b4-4cee-a1f2-10bee77a28e6
title: D3DX10CreateShaderResourceViewFromMemory, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ca3cf26d54d37ab3e3a2141ba7c3e4ea9fdd533f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761972"
---
# <a name="d3dx10createshaderresourceviewfrommemory-function"></a><span data-ttu-id="5bedd-103">D3DX10CreateShaderResourceViewFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="5bedd-103">D3DX10CreateShaderResourceViewFromMemory function</span></span>

<span data-ttu-id="5bedd-104">Créer un affichage des ressources de nuanceur à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="5bedd-104">Create a shader-resource view from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bedd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bedd-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromMemory(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCVOID                  pSrcData,
  _In_  SIZE_T                   SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="5bedd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bedd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bedd-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="5bedd-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="5bedd-109">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui utilisera la ressource.</span><span class="sxs-lookup"><span data-stu-id="5bedd-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-110">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-111">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bedd-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bedd-112">Pointeur vers le fichier en mémoire qui contient l’affichage des ressources du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="5bedd-112">Pointer to the file in memory that contains the shader-resource view.</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-113">*SrcDataSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-114">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bedd-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bedd-115">Taille du fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="5bedd-115">Size of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-116">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-117">Type : **[ **\_ \_ \_ informations sur le chargement de l’image d3dx10**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5bedd-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="5bedd-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5bedd-118">Optional.</span></span> <span data-ttu-id="5bedd-119">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ d3dx10**](d3dx10-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="5bedd-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-120">*pPump* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-121">Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="5bedd-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="5bedd-122">Pointeur vers une interface de pompage de thread (voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="5bedd-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="5bedd-123">Si **null** est spécifié, cette fonction se comportera de façon synchrone et ne sera pas retournée jusqu’à ce qu’elle soit terminée.</span><span class="sxs-lookup"><span data-stu-id="5bedd-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-124">*ppShaderResourceView* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-124">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-125">Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="5bedd-125">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="5bedd-126">Adresse d’un pointeur vers l’affichage des ressources de nuanceur nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="5bedd-126">Address of a pointer to the newly created shader resource view.</span></span> <span data-ttu-id="5bedd-127">Voir [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="5bedd-127">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="5bedd-128">*pHResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5bedd-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bedd-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="5bedd-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="5bedd-130">Pointeur vers la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5bedd-130">A pointer to the return value.</span></span> <span data-ttu-id="5bedd-131">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5bedd-131">May be **NULL**.</span></span> <span data-ttu-id="5bedd-132">Si *pPump* n’a pas la **valeur null**, *pHResult* doit être un emplacement de mémoire valide jusqu’à ce que l’exécution asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="5bedd-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bedd-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bedd-133">Return value</span></span>

<span data-ttu-id="5bedd-134">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bedd-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bedd-135">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5bedd-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bedd-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bedd-136">Requirements</span></span>



| <span data-ttu-id="5bedd-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bedd-137">Requirement</span></span> | <span data-ttu-id="5bedd-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bedd-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bedd-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="5bedd-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5bedd-140"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bedd-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5bedd-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5bedd-141">Library</span></span><br/> | <dl> <span data-ttu-id="5bedd-142"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bedd-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5bedd-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bedd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bedd-144">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="5bedd-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="5bedd-145">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="5bedd-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
