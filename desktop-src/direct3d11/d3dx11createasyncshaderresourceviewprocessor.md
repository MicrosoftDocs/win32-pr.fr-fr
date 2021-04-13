---
title: D3DX11CreateAsyncShaderResourceViewProcessor, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.'
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Fonction D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992288"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="96d77-104">D3DX11CreateAsyncShaderResourceViewProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="96d77-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="96d77-105">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="96d77-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="96d77-106">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="96d77-106">See Remarks.</span></span>

 

<span data-ttu-id="96d77-107">Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="96d77-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="96d77-108">Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX11 qui utilise des [**pompes de thread**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="96d77-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="96d77-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96d77-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="96d77-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96d77-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d77-111">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96d77-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d77-112">Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="96d77-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="96d77-113">Pointeur vers le périphérique Direct3D (voir [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui sera utilisé pour créer une ressource et une vue de ressource Shader pour cette ressource.</span><span class="sxs-lookup"><span data-stu-id="96d77-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="96d77-114">*pLoadInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="96d77-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d77-115">Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="96d77-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="96d77-116">facultatif.</span><span class="sxs-lookup"><span data-stu-id="96d77-116">Optional.</span></span> <span data-ttu-id="96d77-117">Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.</span><span class="sxs-lookup"><span data-stu-id="96d77-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="96d77-118">*ppDataProcessor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="96d77-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d77-119">Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="96d77-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="96d77-120">Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="96d77-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d77-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="96d77-121">Return value</span></span>

<span data-ttu-id="96d77-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96d77-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96d77-123">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="96d77-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96d77-124">Notes</span><span class="sxs-lookup"><span data-stu-id="96d77-124">Remarks</span></span>

<span data-ttu-id="96d77-125">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="96d77-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="96d77-126">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="96d77-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="96d77-127">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="96d77-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d77-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="96d77-128">Requirements</span></span>



| <span data-ttu-id="96d77-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96d77-129">Requirement</span></span> | <span data-ttu-id="96d77-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="96d77-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d77-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="96d77-131">Header</span></span><br/>  | <dl> <span data-ttu-id="96d77-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="96d77-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="96d77-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="96d77-133">Library</span></span><br/> | <dl> <span data-ttu-id="96d77-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96d77-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="96d77-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96d77-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d77-136">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="96d77-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

