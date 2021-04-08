---
description: Charge un maillage à partir d’une ressource.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: D3DXLoadMeshFromXResource, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762031"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="597cb-103">D3DXLoadMeshFromXResource fonction)</span><span class="sxs-lookup"><span data-stu-id="597cb-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="597cb-104">Charge un maillage à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="597cb-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="597cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="597cb-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="597cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="597cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="597cb-107">*Module* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="597cb-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="597cb-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="597cb-109">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="597cb-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="597cb-110">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="597cb-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-111">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="597cb-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="597cb-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="597cb-113">Pointeur vers une chaîne qui spécifie la ressource à partir de laquelle créer le maillage.</span><span class="sxs-lookup"><span data-stu-id="597cb-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="597cb-114">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="597cb-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-115">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="597cb-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-116">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="597cb-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="597cb-117">Pointeur vers une chaîne qui spécifie le type de ressource.</span><span class="sxs-lookup"><span data-stu-id="597cb-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="597cb-118">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="597cb-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-119">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="597cb-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="597cb-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="597cb-121">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) qui spécifient les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="597cb-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-122">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="597cb-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-123">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="597cb-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="597cb-124">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="597cb-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-125">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="597cb-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-126">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="597cb-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="597cb-127">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="597cb-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="597cb-128">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="597cb-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-129">*ppMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="597cb-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="597cb-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="597cb-131">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="597cb-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="597cb-132">Lorsque cette méthode est retournée, ce paramètre est rempli avec un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations enregistrées dans le fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="597cb-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-133">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="597cb-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-134">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="597cb-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="597cb-135">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="597cb-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="597cb-136">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="597cb-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="597cb-137">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="597cb-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="597cb-138">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="597cb-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="597cb-139">*pNumMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="597cb-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-140">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="597cb-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="597cb-141">Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="597cb-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="597cb-142">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="597cb-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597cb-143">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="597cb-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="597cb-144">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="597cb-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="597cb-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="597cb-145">Return value</span></span>

<span data-ttu-id="597cb-146">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="597cb-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="597cb-147">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="597cb-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="597cb-148">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="597cb-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="597cb-149">Notes</span><span class="sxs-lookup"><span data-stu-id="597cb-149">Remarks</span></span>

<span data-ttu-id="597cb-150">Consultez [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) pour en savoir plus sur les paramètres de module, de nom et de type.</span><span class="sxs-lookup"><span data-stu-id="597cb-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="597cb-151">Tous les maillages du fichier seront réduits en un seul maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="597cb-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="597cb-152">Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.</span><span class="sxs-lookup"><span data-stu-id="597cb-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="597cb-153">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="597cb-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="597cb-154">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="597cb-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="597cb-155">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="597cb-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="597cb-156">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="597cb-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="597cb-157">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="597cb-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="597cb-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="597cb-158">Requirements</span></span>



| <span data-ttu-id="597cb-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="597cb-159">Requirement</span></span> | <span data-ttu-id="597cb-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="597cb-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="597cb-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="597cb-161">Header</span></span><br/>  | <dl> <span data-ttu-id="597cb-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="597cb-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="597cb-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="597cb-163">Library</span></span><br/> | <dl> <span data-ttu-id="597cb-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="597cb-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="597cb-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="597cb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597cb-166">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="597cb-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="597cb-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="597cb-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="597cb-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="597cb-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
