---
description: D3DXLoadMeshHierarchyFromXInMemory fonction-charge la première hiérarchie d’images à partir d’un fichier. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: D3DXLoadMeshHierarchyFromXInMemory, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098207"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="38ff2-103">D3DXLoadMeshHierarchyFromXInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="38ff2-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="38ff2-104">Charge la première hiérarchie d’images à partir d’un fichier. x.</span><span class="sxs-lookup"><span data-stu-id="38ff2-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ff2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38ff2-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="38ff2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ff2-107">*pMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38ff2-109">Pointeur vers une mémoire tampon qui contient la hiérarchie de maillage.</span><span class="sxs-lookup"><span data-stu-id="38ff2-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-110">*SizeOfMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38ff2-112">Taille de la mémoire tampon pMemory, en octets.</span><span class="sxs-lookup"><span data-stu-id="38ff2-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-113">*MeshOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38ff2-115">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) qui spécifient les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="38ff2-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-116">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-117">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="38ff2-118">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="38ff2-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-119">*pAlloc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-120">Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="38ff2-121">Pointeur vers une interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="38ff2-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-122">*pUserDataLoader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-123">Type : **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="38ff2-124">Interface fournie par l’application qui permet le chargement des données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38ff2-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="38ff2-125">Consultez [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="38ff2-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-126">*ppFrameHeirarchy* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-127">Type : **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="38ff2-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="38ff2-128">Retourne un pointeur vers la hiérarchie de frames chargée.</span><span class="sxs-lookup"><span data-stu-id="38ff2-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="38ff2-129">Consultez [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="38ff2-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="38ff2-130">*ppAnimController* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="38ff2-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ff2-131">Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="38ff2-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="38ff2-132">Retourne un pointeur vers le contrôleur d’animation correspondant à l’animation dans le fichier. x.</span><span class="sxs-lookup"><span data-stu-id="38ff2-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="38ff2-133">Il est créé avec des suivis et des événements par défaut.</span><span class="sxs-lookup"><span data-stu-id="38ff2-133">This is created with default tracks and events.</span></span> <span data-ttu-id="38ff2-134">Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="38ff2-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ff2-135">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38ff2-135">Return value</span></span>

<span data-ttu-id="38ff2-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38ff2-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38ff2-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38ff2-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38ff2-138">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="38ff2-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ff2-139">Notes </span><span class="sxs-lookup"><span data-stu-id="38ff2-139">Remarks</span></span>

<span data-ttu-id="38ff2-140">Tous les maillages du fichier seront réduits en un seul maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="38ff2-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="38ff2-141">Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.</span><span class="sxs-lookup"><span data-stu-id="38ff2-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ff2-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38ff2-142">Requirements</span></span>



| <span data-ttu-id="38ff2-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38ff2-143">Requirement</span></span> | <span data-ttu-id="38ff2-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="38ff2-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ff2-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="38ff2-145">Header</span></span><br/>  | <dl> <span data-ttu-id="38ff2-146"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="38ff2-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="38ff2-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="38ff2-147">Library</span></span><br/> | <dl> <span data-ttu-id="38ff2-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38ff2-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38ff2-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38ff2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ff2-150">Fonctions d’animation</span><span class="sxs-lookup"><span data-stu-id="38ff2-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
