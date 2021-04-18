---
description: Filtre les niveaux de mipmap d’une texture.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: D3DXFilterTexture, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522958"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="36d98-103">D3DXFilterTexture fonction)</span><span class="sxs-lookup"><span data-stu-id="36d98-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="36d98-104">Filtre les niveaux de mipmap d’une texture.</span><span class="sxs-lookup"><span data-stu-id="36d98-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36d98-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="36d98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d98-107">*pBaseTexture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36d98-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d98-108">Type : **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="36d98-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="36d98-109">Pointeur vers une interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) qui représente l’objet de texture à filtrer.</span><span class="sxs-lookup"><span data-stu-id="36d98-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="36d98-110">*pPalette* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="36d98-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d98-111">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="36d98-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="36d98-112">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) qui représente une palette de couleurs 256 à remplir, ou **null** pour les formats nonpalettized.</span><span class="sxs-lookup"><span data-stu-id="36d98-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="36d98-113">Si aucune palette n’est spécifiée, la palette Direct3D par défaut (une palette blanche opaque) est fournie.</span><span class="sxs-lookup"><span data-stu-id="36d98-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="36d98-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="36d98-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="36d98-115">*SrcLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36d98-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d98-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d98-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d98-117">Niveau dont l’image est utilisée pour générer les niveaux suivants.</span><span class="sxs-lookup"><span data-stu-id="36d98-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="36d98-118">La spécification \_ de la valeur par défaut D3DX pour ce paramètre équivaut à spécifier 0.</span><span class="sxs-lookup"><span data-stu-id="36d98-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="36d98-119">*MipFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36d98-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d98-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d98-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d98-121">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont le mipmap est filtré.</span><span class="sxs-lookup"><span data-stu-id="36d98-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="36d98-122">La spécification \_ de la valeur D3DX par défaut pour ce paramètre est l’équivalent de la spécification de la \_ zone de filtre D3DX \_ si la taille de la texture est une puissance de deux et le filtre de la zone de filtre D3DX dans le \_ \_ \| \_ \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="36d98-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d98-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36d98-123">Return value</span></span>

<span data-ttu-id="36d98-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36d98-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36d98-125">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36d98-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="36d98-126">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="36d98-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="36d98-127">Notes</span><span class="sxs-lookup"><span data-stu-id="36d98-127">Remarks</span></span>

<span data-ttu-id="36d98-128">Un filtre est appliqué de manière récursive à chaque niveau de texture pour générer le niveau de texture suivant.</span><span class="sxs-lookup"><span data-stu-id="36d98-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="36d98-129">L’écriture sur une surface non-niveau zéro de la texture n’entraîne pas la mise à jour du rectangle modifié.</span><span class="sxs-lookup"><span data-stu-id="36d98-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="36d98-130">Si **D3DXFilterTexture** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur la texture.</span><span class="sxs-lookup"><span data-stu-id="36d98-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="36d98-131">Les textures créées dans le pool par défaut (D3DPOOL \_ par défaut) ne peuvent pas être utilisées avec **D3DXFilterTexture** (sauf si elles sont créées avec D3DUSAGE \_ Dynamic), car une opération de verrouillage est nécessaire sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="36d98-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="36d98-132">Notez que les verrous sont interdits sur les textures dans le pool par défaut (sauf s’ils sont dynamiques).</span><span class="sxs-lookup"><span data-stu-id="36d98-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="36d98-133">Pour plus d’informations sur [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="36d98-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="36d98-134">Notez que à compter de DirectX 8,0, le membre peFlags de la structure **PaletteEntry** ne fonctionne pas comme décrit dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="36d98-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="36d98-135">Le membre peFlags est maintenant le canal alpha pour les formats en palette de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="36d98-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="36d98-136">Il n’existe qu’une seule fonction de filtrage de texture, mais deux macros qui appellent cette méthode.</span><span class="sxs-lookup"><span data-stu-id="36d98-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="36d98-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36d98-137">Requirements</span></span>



| <span data-ttu-id="36d98-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36d98-138">Requirement</span></span> | <span data-ttu-id="36d98-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="36d98-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36d98-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="36d98-140">Header</span></span><br/>  | <dl> <span data-ttu-id="36d98-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d98-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="36d98-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="36d98-142">Library</span></span><br/> | <dl> <span data-ttu-id="36d98-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d98-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="36d98-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36d98-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d98-145">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="36d98-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
