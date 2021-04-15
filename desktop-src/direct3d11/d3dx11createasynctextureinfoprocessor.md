---
title: D3DX11CreateAsyncTextureInfoProcessor, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créez un processeur de données à utiliser avec une pompe de thread. | D3DX11CreateAsyncTextureInfoProcessor, fonction (D3DX11tex. h)'
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- Fonction D3DX11CreateAsyncTextureInfoProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992292"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="a6fe1-107">D3DX11CreateAsyncTextureInfoProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="a6fe1-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="a6fe1-108">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="a6fe1-109">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-109">See Remarks.</span></span>

 

<span data-ttu-id="a6fe1-110">Créez un processeur de données à utiliser avec une [**pompe de thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="a6fe1-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fe1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6fe1-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a6fe1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6fe1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fe1-113">*pImageInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a6fe1-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6fe1-114">Type : **[ **\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6fe1-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="a6fe1-115">facultatif.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-115">Optional.</span></span> <span data-ttu-id="a6fe1-116">Identifie les caractéristiques d’une texture (voir [**\_ \_ informations sur l’image D3DX11**](d3dx11-image-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a6fe1-117">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a6fe1-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6fe1-118">Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a6fe1-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a6fe1-119">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a6fe1-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fe1-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a6fe1-120">Return value</span></span>

<span data-ttu-id="a6fe1-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6fe1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6fe1-122">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a6fe1-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a6fe1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a6fe1-123">Remarks</span></span>

<span data-ttu-id="a6fe1-124">Cette API crée une interface de processeur de données. [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) crée l’interface du processeur de données et charge la texture.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="a6fe1-125">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="a6fe1-126">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="a6fe1-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="a6fe1-127">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a6fe1-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6fe1-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a6fe1-128">Requirements</span></span>



| <span data-ttu-id="a6fe1-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6fe1-129">Requirement</span></span> | <span data-ttu-id="a6fe1-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6fe1-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fe1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6fe1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a6fe1-132"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6fe1-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a6fe1-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a6fe1-133">Library</span></span><br/> | <dl> <span data-ttu-id="a6fe1-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6fe1-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a6fe1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6fe1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fe1-136">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="a6fe1-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

