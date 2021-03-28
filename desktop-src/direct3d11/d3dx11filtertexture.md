---
title: D3DX11FilterTexture, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez qu’au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque DirectXTex, GenerateMipMaps et GenerateMipMaps3D. Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.'
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- Fonction D3DX11FilterTexture Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974599"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="a784b-106">D3DX11FilterTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="a784b-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="a784b-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a784b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a784b-108">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [DirectXTex](https://github.com/Microsoft/DirectXTex) , **GenerateMipMaps** et **GenerateMipMaps3D**.</span><span class="sxs-lookup"><span data-stu-id="a784b-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="a784b-109">Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.</span><span class="sxs-lookup"><span data-stu-id="a784b-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a784b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a784b-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="a784b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a784b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a784b-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="a784b-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-113">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="a784b-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="a784b-114">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="a784b-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="a784b-115">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="a784b-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-116">Type : **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="a784b-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="a784b-117">Objet de texture à filtrer.</span><span class="sxs-lookup"><span data-stu-id="a784b-117">The texture object to be filtered.</span></span> <span data-ttu-id="a784b-118">Consultez [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="a784b-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="a784b-119">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="a784b-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a784b-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a784b-121">Niveau de mipmap dont les données sont utilisées pour générer le reste de la chaîne mipmap.</span><span class="sxs-lookup"><span data-stu-id="a784b-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="a784b-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="a784b-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="a784b-123">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a784b-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a784b-124">Indicateurs contrôlant la manière dont chaque miplevel est filtré (ou D3DX11 \_ par défaut pour le \_ filtre D3DX11 \_ linéaire).</span><span class="sxs-lookup"><span data-stu-id="a784b-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="a784b-125">Consultez [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="a784b-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a784b-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a784b-126">Return value</span></span>

<span data-ttu-id="a784b-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a784b-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a784b-128">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a784b-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a784b-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a784b-129">Requirements</span></span>



| <span data-ttu-id="a784b-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a784b-130">Requirement</span></span> | <span data-ttu-id="a784b-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a784b-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a784b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a784b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a784b-133"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a784b-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a784b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a784b-134">Library</span></span><br/> | <dl> <span data-ttu-id="a784b-135"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a784b-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a784b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a784b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a784b-137">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="a784b-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

