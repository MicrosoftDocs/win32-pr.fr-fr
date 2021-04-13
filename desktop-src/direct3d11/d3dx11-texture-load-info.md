---
title: Structure D3DX11_TEXTURE_LOAD_INFO (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.'
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- Structure D3DX11_TEXTURE_LOAD_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992312"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="467e5-105">\_Structure d' \_ \_ informations sur le chargement de la texture D3DX11</span><span class="sxs-lookup"><span data-stu-id="467e5-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="467e5-106">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="467e5-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="467e5-107">Décrit les paramètres utilisés pour charger une texture à partir d’une autre texture.</span><span class="sxs-lookup"><span data-stu-id="467e5-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="467e5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="467e5-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="467e5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="467e5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="467e5-110">**pSrcBox**</span><span class="sxs-lookup"><span data-stu-id="467e5-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-111">Type : **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="467e5-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="467e5-112">Zone texture source (consultez [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="467e5-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="467e5-113">**pDstBox**</span><span class="sxs-lookup"><span data-stu-id="467e5-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-114">Type : **[ **d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="467e5-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="467e5-115">Zone texture de destination (voir [**d3d11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="467e5-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="467e5-116">**SrcFirstMip**</span><span class="sxs-lookup"><span data-stu-id="467e5-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-118">Niveau de mipmap de la texture source, consultez [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="467e5-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-119">**DstFirstMip**</span><span class="sxs-lookup"><span data-stu-id="467e5-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-120">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-121">Niveau de mipmap de texture de destination, consultez [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="467e5-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-122">**NumMips**</span><span class="sxs-lookup"><span data-stu-id="467e5-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-123">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-124">Nombre de niveaux de mipmap dans la texture source.</span><span class="sxs-lookup"><span data-stu-id="467e5-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-125">**SrcFirstElement**</span><span class="sxs-lookup"><span data-stu-id="467e5-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-126">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-127">Premier élément de la texture source.</span><span class="sxs-lookup"><span data-stu-id="467e5-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-128">**DstFirstElement**</span><span class="sxs-lookup"><span data-stu-id="467e5-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-129">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-130">Premier élément de la texture de destination.</span><span class="sxs-lookup"><span data-stu-id="467e5-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="467e5-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-132">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-133">Nombre d’éléments à charger.</span><span class="sxs-lookup"><span data-stu-id="467e5-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="467e5-134">**Filter**</span><span class="sxs-lookup"><span data-stu-id="467e5-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-135">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-136">Options de filtrage pendant le rééchantillonnage (voir [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="467e5-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="467e5-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="467e5-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="467e5-138">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="467e5-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="467e5-139">Options de filtrage lors de la génération de niveaux MIP (voir [**\_ \_ indicateur de filtre D3DX11**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="467e5-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="467e5-140">Notes</span><span class="sxs-lookup"><span data-stu-id="467e5-140">Remarks</span></span>

<span data-ttu-id="467e5-141">Cette structure est utilisée dans un appel à [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span><span class="sxs-lookup"><span data-stu-id="467e5-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="467e5-142">Les valeurs par défaut sont :</span><span class="sxs-lookup"><span data-stu-id="467e5-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="467e5-143">Spécifications</span><span class="sxs-lookup"><span data-stu-id="467e5-143">Requirements</span></span>



| <span data-ttu-id="467e5-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="467e5-144">Requirement</span></span> | <span data-ttu-id="467e5-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="467e5-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="467e5-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="467e5-146">Header</span></span><br/> | <dl> <span data-ttu-id="467e5-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="467e5-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="467e5-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="467e5-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467e5-149">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="467e5-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

