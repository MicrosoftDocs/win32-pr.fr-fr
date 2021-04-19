---
description: Charge une maille à partir de la mémoire.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: D3DXLoadMeshFromXInMemory, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532441"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="b0914-103">D3DXLoadMeshFromXInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="b0914-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="b0914-104">Charge une maille à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b0914-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0914-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0914-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="b0914-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0914-107">*Mémoire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0914-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-108">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0914-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0914-109">Pointeur vers la mémoire tampon qui contient les données de maillage.</span><span class="sxs-lookup"><span data-stu-id="b0914-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-110">*SizeOfMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0914-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0914-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0914-112">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="b0914-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-113">*Options* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0914-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0914-115">Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="b0914-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-116">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0914-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-117">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b0914-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b0914-118">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="b0914-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-119">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-120">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0914-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0914-121">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b0914-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="b0914-122">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="b0914-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-123">*ppMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-124">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0914-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0914-125">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b0914-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="b0914-126">Lorsque cette méthode est retournée, ce paramètre est rempli avec un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations enregistrées dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="b0914-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-127">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-128">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0914-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0914-129">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="b0914-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="b0914-130">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="b0914-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="b0914-131">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="b0914-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="b0914-132">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b0914-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0914-133">*pNumMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0914-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0914-135">Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="b0914-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="b0914-136">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0914-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0914-137">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0914-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b0914-138">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="b0914-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0914-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0914-139">Return value</span></span>

<span data-ttu-id="b0914-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0914-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0914-141">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0914-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0914-142">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="b0914-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0914-143">Notes</span><span class="sxs-lookup"><span data-stu-id="b0914-143">Remarks</span></span>

<span data-ttu-id="b0914-144">Tous les maillages du fichier seront réduits en un seul maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="b0914-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="b0914-145">Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.</span><span class="sxs-lookup"><span data-stu-id="b0914-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="b0914-146">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="b0914-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="b0914-147">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="b0914-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="b0914-148">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="b0914-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="b0914-149">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="b0914-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="b0914-150">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="b0914-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0914-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0914-151">Requirements</span></span>



| <span data-ttu-id="b0914-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0914-152">Requirement</span></span> | <span data-ttu-id="b0914-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0914-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0914-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0914-154">Header</span></span><br/>  | <dl> <span data-ttu-id="b0914-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0914-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b0914-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0914-156">Library</span></span><br/> | <dl> <span data-ttu-id="b0914-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0914-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0914-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0914-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0914-159">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="b0914-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="b0914-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b0914-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="b0914-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="b0914-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
