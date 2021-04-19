---
description: Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: D3DX10FilterTexture, fonction (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537234"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="2a3e9-103">D3DX10FilterTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="2a3e9-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="2a3e9-104">Génère une chaîne mipmap à l’aide d’un filtre de texture particulier.</span><span class="sxs-lookup"><span data-stu-id="2a3e9-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a3e9-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="2a3e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a3e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a3e9-107">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="2a3e9-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="2a3e9-108">Type : **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="2a3e9-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="2a3e9-109">Objet de texture à filtrer.</span><span class="sxs-lookup"><span data-stu-id="2a3e9-109">The texture object to be filtered.</span></span> <span data-ttu-id="2a3e9-110">Consultez [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="2a3e9-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="2a3e9-111">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="2a3e9-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="2a3e9-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a3e9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a3e9-113">Niveau de mipmap dont les données sont utilisées pour générer le reste de la chaîne mipmap.</span><span class="sxs-lookup"><span data-stu-id="2a3e9-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="2a3e9-114">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="2a3e9-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="2a3e9-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a3e9-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a3e9-116">Indicateurs contrôlant la manière dont chaque miplevel est filtré (ou D3DX10 \_ par défaut pour \_ la zone de filtre d3dx10 \_ ).</span><span class="sxs-lookup"><span data-stu-id="2a3e9-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="2a3e9-117">Consultez [**\_ \_ indicateur de filtre d3dx10**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="2a3e9-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a3e9-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a3e9-118">Return value</span></span>

<span data-ttu-id="2a3e9-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a3e9-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a3e9-120">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2a3e9-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3e9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a3e9-121">Requirements</span></span>



| <span data-ttu-id="2a3e9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a3e9-122">Requirement</span></span> | <span data-ttu-id="2a3e9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a3e9-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3e9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a3e9-124">Header</span></span><br/> | <dl> <span data-ttu-id="2a3e9-125"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3e9-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a3e9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3e9-127">Fonctions de texture dans D3DX 10</span><span class="sxs-lookup"><span data-stu-id="2a3e9-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
