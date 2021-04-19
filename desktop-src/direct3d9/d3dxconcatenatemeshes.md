---
description: Concatène un groupe de maillages dans un maillage commun. Cette méthode peut éventuellement appliquer une transformation de matrice à chaque maillage d’entrée et ses coordonnées de texture.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: D3DXConcatenateMeshes, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531349"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="b15cb-104">D3DXConcatenateMeshes fonction)</span><span class="sxs-lookup"><span data-stu-id="b15cb-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="b15cb-105">Concatène un groupe de maillages dans un maillage commun.</span><span class="sxs-lookup"><span data-stu-id="b15cb-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="b15cb-106">Cette méthode peut éventuellement appliquer une transformation de matrice à chaque maillage d’entrée et ses coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="b15cb-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15cb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b15cb-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="b15cb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b15cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15cb-109">*ppMeshes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b15cb-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b15cb-111">Tableau de pointeurs de maillage d’entrée (consultez [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="b15cb-112">Le nombre d’éléments dans le tableau est NumMeshes.</span><span class="sxs-lookup"><span data-stu-id="b15cb-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-113">*NumMeshes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b15cb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b15cb-115">Nombre de maillages d’entrée à concaténer.</span><span class="sxs-lookup"><span data-stu-id="b15cb-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-116">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b15cb-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b15cb-118">Options de création de maillage ; Il s’agit d’une combinaison d’un ou plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="b15cb-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="b15cb-119">Les options de création de maillage sont équivalentes au paramètre d’options requis par [**D3DXCreateMesh**](d3dxcreatemesh.md).</span><span class="sxs-lookup"><span data-stu-id="b15cb-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-120">*pGeomXForms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-121">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b15cb-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b15cb-122">Tableau facultatif de transformations géométriques.</span><span class="sxs-lookup"><span data-stu-id="b15cb-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="b15cb-123">Le nombre d’éléments dans le tableau est NumMeshes ; chaque élément est une matrice de transformation (consultez [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="b15cb-124">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b15cb-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-125">*pTextureXForms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-126">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b15cb-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b15cb-127">Tableau facultatif de transformations de texture.</span><span class="sxs-lookup"><span data-stu-id="b15cb-127">Optional array of texture transforms.</span></span> <span data-ttu-id="b15cb-128">Le nombre d’éléments dans le tableau est NumMeshes ; chaque élément est une matrice de transformation (consultez [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="b15cb-129">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b15cb-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-130">*pDecl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-131">Type : **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="b15cb-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="b15cb-132">Pointeur facultatif vers une déclaration de vertex (consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="b15cb-133">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b15cb-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-134">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-135">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b15cb-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b15cb-136">Pointeur vers un appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour créer le nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="b15cb-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b15cb-137">*ppMeshOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b15cb-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b15cb-138">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b15cb-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b15cb-139">Adresse d’un pointeur vers la maille créée (voir [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15cb-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b15cb-140">Return value</span></span>

<span data-ttu-id="b15cb-141">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b15cb-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b15cb-142">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b15cb-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b15cb-143">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b15cb-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15cb-144">Notes</span><span class="sxs-lookup"><span data-stu-id="b15cb-144">Remarks</span></span>

<span data-ttu-id="b15cb-145">Si aucune [déclaration de vertex](vertex-declaration.md) n’est fournie dans le cadre du paramètre de création de maillage d’options, la méthode génère une Union de toutes les déclarations de vertex des sous-mailles, en promouvant les canaux et les types si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b15cb-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="b15cb-146">La méthode crée une table d’attributs à partir des tables d’attributs des maillages d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b15cb-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="b15cb-147">Pour garantir la création d’une table d’attributs, appelez [**optimize**](id3dxmesh--optimize.md) avec les indicateurs définis sur D3DXMESHOPT \_ compact et D3DXMESHOPT \_ ATTRSORT (voir [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="b15cb-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b15cb-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b15cb-148">Requirements</span></span>



| <span data-ttu-id="b15cb-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b15cb-149">Requirement</span></span> | <span data-ttu-id="b15cb-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="b15cb-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b15cb-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="b15cb-151">Header</span></span><br/>  | <dl> <span data-ttu-id="b15cb-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b15cb-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b15cb-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b15cb-153">Library</span></span><br/> | <dl> <span data-ttu-id="b15cb-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b15cb-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b15cb-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b15cb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15cb-156">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b15cb-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
