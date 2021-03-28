---
title: D3DX11CreateAsyncResourceLoader, fonction (D3DX11async. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Consultez la section Notes. Créez un chargeur de ressources asynchrones.'
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- Fonction D3DX11CreateAsyncResourceLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043148"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="30baa-106">D3DX11CreateAsyncResourceLoader fonction)</span><span class="sxs-lookup"><span data-stu-id="30baa-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="30baa-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="30baa-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="30baa-108">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="30baa-108">See Remarks.</span></span>

 

<span data-ttu-id="30baa-109">Créez un chargeur de ressources asynchrones.</span><span class="sxs-lookup"><span data-stu-id="30baa-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="30baa-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30baa-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="30baa-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30baa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30baa-112">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30baa-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30baa-113">Type : **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30baa-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30baa-114">Handle du module de ressources.</span><span class="sxs-lookup"><span data-stu-id="30baa-114">Handle to the resource module.</span></span> <span data-ttu-id="30baa-115">Utilisez la [fonction GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour récupérer le descripteur.</span><span class="sxs-lookup"><span data-stu-id="30baa-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="30baa-116">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30baa-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30baa-117">Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30baa-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30baa-118">Nom de la ressource dans hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="30baa-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="30baa-119">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="30baa-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="30baa-120">Dans le cas contraire, le type de données est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="30baa-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="30baa-121">*ppDataLoader* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30baa-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30baa-122">Type : **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="30baa-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="30baa-123">Adresse d’un pointeur vers le chargeur de données asynchrones (voir [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="30baa-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30baa-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30baa-124">Return value</span></span>

<span data-ttu-id="30baa-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30baa-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30baa-126">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="30baa-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30baa-127">Notes</span><span class="sxs-lookup"><span data-stu-id="30baa-127">Remarks</span></span>

<span data-ttu-id="30baa-128">Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="30baa-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="30baa-129">Pour les applications du Windows Store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le modèle de programmation asynchrone Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="30baa-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="30baa-130">Pour les applications de bureau Win32, vous pouvez utiliser le [Runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.</span><span class="sxs-lookup"><span data-stu-id="30baa-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="30baa-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="30baa-131">Requirements</span></span>



| <span data-ttu-id="30baa-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30baa-132">Requirement</span></span> | <span data-ttu-id="30baa-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="30baa-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30baa-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="30baa-134">Header</span></span><br/>  | <dl> <span data-ttu-id="30baa-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="30baa-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="30baa-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30baa-136">Library</span></span><br/> | <dl> <span data-ttu-id="30baa-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30baa-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="30baa-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30baa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30baa-139">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="30baa-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

