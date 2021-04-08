---
description: Crée un mappage d’environnement de rendu.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: D3DXCreateRenderToEnvMap, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043104"
---
# <a name="d3dxcreaterendertoenvmap-function"></a><span data-ttu-id="14441-103">D3DXCreateRenderToEnvMap fonction)</span><span class="sxs-lookup"><span data-stu-id="14441-103">D3DXCreateRenderToEnvMap function</span></span>

<span data-ttu-id="14441-104">Crée un mappage d’environnement de rendu.</span><span class="sxs-lookup"><span data-stu-id="14441-104">Creates a render environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="14441-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14441-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a><span data-ttu-id="14441-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14441-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14441-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="14441-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="14441-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , qui est l’appareil à associer à la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="14441-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, which is the device to associate with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="14441-110">*Taille* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14441-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14441-112">Taille de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="14441-112">Size of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="14441-113">*Miplevels a* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-113">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14441-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14441-115">Nombre de niveaux de mipmap.</span><span class="sxs-lookup"><span data-stu-id="14441-115">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="14441-116">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-117">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="14441-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="14441-118">Membre du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le format de pixel de la carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="14441-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the pixel format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="14441-119">*DepthStencil* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-120">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14441-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14441-121">Si la **valeur est true**, la surface de rendu prend en charge une surface de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="14441-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="14441-122">Dans le cas contraire, ce membre est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="14441-122">Otherwise, this member is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="14441-123">*DepthStencilFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14441-123">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-124">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="14441-124">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="14441-125">Si DepthStencil a la valeur **true**, ce paramètre est un membre du type énuméré [D3DFORMAT](d3dformat.md) qui décrit le format de stencil de profondeur de la carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="14441-125">If DepthStencil is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type that describes the depth-stencil format of the environment map.</span></span>

</dd> <dt>

<span data-ttu-id="14441-126">*ppRenderToEnvMap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14441-126">*ppRenderToEnvMap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14441-127">Type : **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span><span class="sxs-lookup"><span data-stu-id="14441-127">Type: **[**LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***</span></span>

<span data-ttu-id="14441-128">Adresse d’un pointeur vers une interface [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) qui représente le mappage d’environnement de rendu créé.</span><span class="sxs-lookup"><span data-stu-id="14441-128">Address of a pointer to an [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) interface that represents the created render environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14441-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14441-129">Return value</span></span>

<span data-ttu-id="14441-130">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14441-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14441-131">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14441-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14441-132">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="14441-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="14441-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14441-133">Requirements</span></span>



| <span data-ttu-id="14441-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14441-134">Requirement</span></span> | <span data-ttu-id="14441-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="14441-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14441-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="14441-136">Header</span></span><br/>  | <dl> <span data-ttu-id="14441-137"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="14441-137"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="14441-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="14441-138">Library</span></span><br/> | <dl> <span data-ttu-id="14441-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14441-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14441-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14441-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14441-141">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="14441-141">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
