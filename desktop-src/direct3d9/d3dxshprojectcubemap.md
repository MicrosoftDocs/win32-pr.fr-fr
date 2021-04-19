---
description: Projette une fonction représentée sur un mappage de cube dans des harmoniques sphériques (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: D3DXSHProjectCubeMap, fonction (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527126"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="93321-103">D3DXSHProjectCubeMap fonction)</span><span class="sxs-lookup"><span data-stu-id="93321-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="93321-104">Projette une fonction représentée sur un mappage de cube dans des harmoniques sphériques (SH).</span><span class="sxs-lookup"><span data-stu-id="93321-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="93321-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93321-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="93321-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="93321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93321-107">*Commande* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93321-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93321-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93321-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93321-109">Ordre de l’évaluation de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="93321-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="93321-110">La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="93321-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="93321-111">L’évaluation génère des coefficients de commande ².</span><span class="sxs-lookup"><span data-stu-id="93321-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="93321-112">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="93321-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="93321-113">*pCubeMap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93321-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93321-114">Type : **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="93321-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="93321-115">Pointeur désignant une texture de cube source.</span><span class="sxs-lookup"><span data-stu-id="93321-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="93321-116">Consultez [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="93321-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="93321-117">*pROut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93321-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93321-118">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93321-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93321-119">Pointeur vers le vecteur de sortie SH pour le composant rouge.</span><span class="sxs-lookup"><span data-stu-id="93321-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="93321-120">*pGOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93321-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93321-121">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93321-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93321-122">Pointeur vers le vecteur de sortie SH pour le composant vert.</span><span class="sxs-lookup"><span data-stu-id="93321-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="93321-123">*pBOut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="93321-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93321-124">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="93321-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="93321-125">Pointeur vers le vecteur de sortie SH pour le composant bleu.</span><span class="sxs-lookup"><span data-stu-id="93321-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93321-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="93321-126">Return value</span></span>

<span data-ttu-id="93321-127">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93321-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93321-128">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93321-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="93321-129">Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="93321-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="93321-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93321-130">Requirements</span></span>



| <span data-ttu-id="93321-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93321-131">Requirement</span></span> | <span data-ttu-id="93321-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="93321-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93321-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="93321-133">Header</span></span><br/>  | <dl> <span data-ttu-id="93321-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93321-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="93321-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="93321-135">Library</span></span><br/> | <dl> <span data-ttu-id="93321-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93321-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93321-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93321-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93321-138">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="93321-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="93321-139">Transfert de luminance précalculé (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="93321-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
