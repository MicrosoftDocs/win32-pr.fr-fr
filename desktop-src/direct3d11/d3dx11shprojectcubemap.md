---
title: D3DX11SHProjectCubeMap, fonction (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Notez que, au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque mathématique des harmoniques sphériques, SHProjectCubeMap.'
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- Fonction D3DX11SHProjectCubeMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992260"
---
# <a name="d3dx11shprojectcubemap-function"></a><span data-ttu-id="5d8de-105">D3DX11SHProjectCubeMap fonction)</span><span class="sxs-lookup"><span data-stu-id="5d8de-105">D3DX11SHProjectCubeMap function</span></span>

> [!Note]  
> <span data-ttu-id="5d8de-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5d8de-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d8de-107">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser la bibliothèque [mathématique des harmoniques sphériques](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) , **SHProjectCubeMap**.</span><span class="sxs-lookup"><span data-stu-id="5d8de-107">Instead of using this function, we recommend that you use the [Spherical Harmonics Math](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) library, **SHProjectCubeMap**.</span></span>

 

<span data-ttu-id="5d8de-108">Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="5d8de-108">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8de-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d8de-109">Syntax</span></span>


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5d8de-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d8de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d8de-111">*pContext*</span><span class="sxs-lookup"><span data-stu-id="5d8de-111">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-112">Type : **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="5d8de-112">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="5d8de-113">Pointeur vers un objet [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="5d8de-113">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="5d8de-114">*Commande*</span><span class="sxs-lookup"><span data-stu-id="5d8de-114">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-115">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5d8de-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5d8de-116">Ordre de l’évaluation SH, génère les coefficients de commande ^ 2 dont le degré est la commande-1.</span><span class="sxs-lookup"><span data-stu-id="5d8de-116">Order of the SH evaluation, generates Order^2 coefficients whose degree is Order-1.</span></span> <span data-ttu-id="5d8de-117">La plage valide est comprise entre 2 et 6.</span><span class="sxs-lookup"><span data-stu-id="5d8de-117">Valid range is between 2 and 6.</span></span>

</dd> <dt>

<span data-ttu-id="5d8de-118">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="5d8de-118">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-119">Type : **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="5d8de-119">Type: **[**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***</span></span>

<span data-ttu-id="5d8de-120">Pointeur vers un [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) qui représente un carte cubique qui va être projeté dans des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="5d8de-120">A pointer to an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) that represents a cubemap that is going to be projected into spherical harmonics.</span></span>

</dd> <dt>

<span data-ttu-id="5d8de-121">*pROut*</span><span class="sxs-lookup"><span data-stu-id="5d8de-121">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-122">Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="5d8de-122">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5d8de-123">Vecteur SH de sortie pour le rouge.</span><span class="sxs-lookup"><span data-stu-id="5d8de-123">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="5d8de-124">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="5d8de-124">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-125">Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="5d8de-125">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5d8de-126">Vecteur SH de sortie pour le vert.</span><span class="sxs-lookup"><span data-stu-id="5d8de-126">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="5d8de-127">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="5d8de-127">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="5d8de-128">Type : **[ **float**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="5d8de-128">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5d8de-129">Vecteur SH de sortie pour le bleu.</span><span class="sxs-lookup"><span data-stu-id="5d8de-129">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d8de-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d8de-130">Return value</span></span>

<span data-ttu-id="5d8de-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d8de-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d8de-132">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5d8de-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d8de-133">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d8de-133">Requirements</span></span>



| <span data-ttu-id="5d8de-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d8de-134">Requirement</span></span> | <span data-ttu-id="5d8de-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d8de-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8de-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d8de-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5d8de-137"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d8de-137"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5d8de-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d8de-138">Library</span></span><br/> | <dl> <span data-ttu-id="5d8de-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d8de-139"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5d8de-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d8de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8de-141">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="5d8de-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

