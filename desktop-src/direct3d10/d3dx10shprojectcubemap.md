---
description: Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: D3DX10SHProjectCubeMap, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525879"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="5540e-103">D3DX10SHProjectCubeMap fonction)</span><span class="sxs-lookup"><span data-stu-id="5540e-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="5540e-104">Projette une fonction représentée dans un mappage de cube dans des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="5540e-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="5540e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5540e-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="5540e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5540e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5540e-107">*Commande*</span><span class="sxs-lookup"><span data-stu-id="5540e-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="5540e-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5540e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5540e-109">Ordre de l’évaluation SH, génère la commande ^ 2 coefs, le degré est Order-1.</span><span class="sxs-lookup"><span data-stu-id="5540e-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="5540e-110">*pCubeMap*</span><span class="sxs-lookup"><span data-stu-id="5540e-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="5540e-111">Type : **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="5540e-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="5540e-112">Carte cubique qui va être projeté dans des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="5540e-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="5540e-113">Consultez [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="5540e-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="5540e-114">*pROut*</span><span class="sxs-lookup"><span data-stu-id="5540e-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="5540e-115">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5540e-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5540e-116">Vecteur SH de sortie pour le rouge.</span><span class="sxs-lookup"><span data-stu-id="5540e-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="5540e-117">*pGOut*</span><span class="sxs-lookup"><span data-stu-id="5540e-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="5540e-118">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5540e-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5540e-119">Vecteur SH de sortie pour le vert.</span><span class="sxs-lookup"><span data-stu-id="5540e-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="5540e-120">*pBOut*</span><span class="sxs-lookup"><span data-stu-id="5540e-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="5540e-121">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5540e-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5540e-122">Vecteur SH de sortie pour le bleu.</span><span class="sxs-lookup"><span data-stu-id="5540e-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5540e-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5540e-123">Return value</span></span>

<span data-ttu-id="5540e-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5540e-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5540e-125">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="5540e-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5540e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5540e-126">Requirements</span></span>



| <span data-ttu-id="5540e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5540e-127">Requirement</span></span> | <span data-ttu-id="5540e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5540e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5540e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5540e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5540e-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5540e-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5540e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5540e-131">Library</span></span><br/> | <dl> <span data-ttu-id="5540e-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5540e-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5540e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5540e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5540e-134">Fonctions mathématiques</span><span class="sxs-lookup"><span data-stu-id="5540e-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
