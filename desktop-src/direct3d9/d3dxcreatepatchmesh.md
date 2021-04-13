---
description: Crée une maille à partir d’un maillage de contrôle-correctif.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: D3DXCreatePatchMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323321"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="4e1af-103">D3DXCreatePatchMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="4e1af-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="4e1af-104">Crée une maille à partir d’un maillage de contrôle-correctif.</span><span class="sxs-lookup"><span data-stu-id="4e1af-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1af-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e1af-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="4e1af-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e1af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1af-107">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-108">Type : **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e1af-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="4e1af-109">Structure des informations sur les correctifs.</span><span class="sxs-lookup"><span data-stu-id="4e1af-109">Patch information structure.</span></span> <span data-ttu-id="4e1af-110">Pour plus d’informations, consultez [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="4e1af-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-111">*dwNumPatches* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e1af-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e1af-113">Nombre de correctifs.</span><span class="sxs-lookup"><span data-stu-id="4e1af-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-114">*dwNumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-115">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e1af-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e1af-116">Nombre de vertex de contrôle dans le correctif.</span><span class="sxs-lookup"><span data-stu-id="4e1af-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-117">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-118">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e1af-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e1af-119">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="4e1af-119">Unused.</span></span> <span data-ttu-id="4e1af-120">Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4e1af-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-121">*pDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-122">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e1af-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4e1af-123">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="4e1af-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-124">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-125">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4e1af-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4e1af-126">Pointeur l’appareil qui crée la maille de correctifs.</span><span class="sxs-lookup"><span data-stu-id="4e1af-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="4e1af-127">Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="4e1af-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="4e1af-128">*pPatchMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4e1af-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1af-129">Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e1af-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="4e1af-130">Pointeur vers l’objet [**ID3DXPatchMesh**](id3dxpatchmesh.md) créé.</span><span class="sxs-lookup"><span data-stu-id="4e1af-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1af-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e1af-131">Return value</span></span>

<span data-ttu-id="4e1af-132">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e1af-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e1af-133">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e1af-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e1af-134">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4e1af-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1af-135">Notes</span><span class="sxs-lookup"><span data-stu-id="4e1af-135">Remarks</span></span>

<span data-ttu-id="4e1af-136">Cette méthode prend une maille de correction d’entrée et la convertit en maillage fractionné.</span><span class="sxs-lookup"><span data-stu-id="4e1af-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="4e1af-137">Les maillages de correctifs utilisent des mémoires tampons d’index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4e1af-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="4e1af-138">Par conséquent, les index de [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) sont de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4e1af-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1af-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e1af-139">Requirements</span></span>



| <span data-ttu-id="4e1af-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e1af-140">Requirement</span></span> | <span data-ttu-id="4e1af-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e1af-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1af-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e1af-142">Header</span></span><br/>  | <dl> <span data-ttu-id="4e1af-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1af-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4e1af-144">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e1af-144">Library</span></span><br/> | <dl> <span data-ttu-id="4e1af-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e1af-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e1af-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e1af-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1af-147">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="4e1af-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="4e1af-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="4e1af-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
