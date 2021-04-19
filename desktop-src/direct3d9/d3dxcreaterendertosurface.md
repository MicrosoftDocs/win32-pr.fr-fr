---
description: Crée une surface de rendu.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: D3DXCreateRenderToSurface, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523829"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="f8ffc-103">D3DXCreateRenderToSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="f8ffc-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="f8ffc-104">Crée une surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ffc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8ffc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="f8ffc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8ffc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ffc-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="f8ffc-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’appareil à associer à la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-110">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8ffc-112">Largeur de la surface de rendu, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-113">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8ffc-115">Hauteur de la surface de rendu, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-116">*Format* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-117">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f8ffc-118">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de pixel de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-119">*DepthStencil* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-120">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8ffc-121">Si la **valeur est true**, la surface de rendu prend en charge une surface de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="f8ffc-122">Dans le cas contraire, ce membre est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="f8ffc-123">Cette fonction crée une nouvelle mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-124">*DepthStencilFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-125">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f8ffc-126">Si *DepthStencil* a la valeur **true**, ce paramètre est un membre du type énuméré [D3DFORMAT](d3dformat.md) , qui décrit le format de stencil de profondeur de la surface de rendu.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="f8ffc-127">*ppRenderToSurface* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8ffc-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ffc-128">Type : **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8ffc-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="f8ffc-129">Adresse d’un pointeur vers une interface [**ID3DXRenderToSurface**](id3dxrendertosurface.md) représentant la surface de rendu créée.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ffc-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8ffc-130">Return value</span></span>

<span data-ttu-id="f8ffc-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8ffc-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8ffc-132">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8ffc-133">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f8ffc-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ffc-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8ffc-134">Requirements</span></span>



| <span data-ttu-id="f8ffc-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8ffc-135">Requirement</span></span> | <span data-ttu-id="f8ffc-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8ffc-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ffc-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8ffc-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ffc-138"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ffc-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ffc-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f8ffc-139">Library</span></span><br/> | <dl> <span data-ttu-id="f8ffc-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ffc-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8ffc-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8ffc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ffc-142">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="f8ffc-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
