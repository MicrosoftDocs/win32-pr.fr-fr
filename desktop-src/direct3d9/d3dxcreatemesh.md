---
description: D3DXCreateMesh fonction-crée un objet de maillage à l’aide d’un déclarateur.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: D3DXCreateMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c7e1c0d626c74f5427f91a5b9eb796e3b79d5a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102757"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="cbc7c-103">D3DXCreateMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="cbc7c-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="cbc7c-104">Crée un objet de maillage à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbc7c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="cbc7c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbc7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc7c-107">*NumFaces* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbc7c-109">Nombre de faces de la maille.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-109">Number of faces for the mesh.</span></span> <span data-ttu-id="cbc7c-110">La plage valide pour ce nombre est supérieure à 0, et une valeur inférieure à la valeur DWORD maximale (généralement 65534), car le dernier index est réservé.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="cbc7c-111">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbc7c-113">Nombre de vertex pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="cbc7c-114">Ce paramètre doit être supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="cbc7c-115">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-116">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cbc7c-117">Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cbc7c-118">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-119">Type : **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="cbc7c-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="cbc7c-120">Tableau d’éléments [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , décrivant le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="cbc7c-121">Ce paramètre doit être directement mappé à un format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="cbc7c-122">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-123">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cbc7c-124">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil à associer à la maille.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cbc7c-125">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cbc7c-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc7c-126">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cbc7c-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cbc7c-127">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant l’objet de maillage créé.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc7c-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cbc7c-128">Return value</span></span>

<span data-ttu-id="cbc7c-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cbc7c-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cbc7c-131">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cbc7c-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc7c-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbc7c-132">Requirements</span></span>



| <span data-ttu-id="cbc7c-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbc7c-133">Requirement</span></span> | <span data-ttu-id="cbc7c-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbc7c-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc7c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbc7c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="cbc7c-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc7c-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cbc7c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cbc7c-137">Library</span></span><br/> | <dl> <span data-ttu-id="cbc7c-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbc7c-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cbc7c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbc7c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc7c-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="cbc7c-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="cbc7c-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="cbc7c-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
