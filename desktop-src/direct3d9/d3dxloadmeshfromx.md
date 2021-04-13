---
description: Charge un maillage à partir d’un fichier DirectX. x.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: D3DXLoadMeshFromX, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322898"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="dea05-103">D3DXLoadMeshFromX fonction)</span><span class="sxs-lookup"><span data-stu-id="dea05-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="dea05-104">Charge un maillage à partir d’un fichier DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="dea05-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea05-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="dea05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dea05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea05-107">*pFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea05-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-108">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dea05-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dea05-109">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="dea05-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="dea05-110">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="dea05-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dea05-111">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="dea05-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="dea05-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="dea05-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dea05-113">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea05-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dea05-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dea05-115">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , qui spécifie les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="dea05-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dea05-116">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dea05-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-117">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="dea05-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="dea05-118">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="dea05-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dea05-119">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea05-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-120">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dea05-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dea05-121">Pointeur vers une mémoire tampon qui contient les données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="dea05-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="dea05-122">Les données d’adjacence contiennent un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="dea05-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="dea05-123">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="dea05-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="dea05-124">*ppMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea05-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dea05-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dea05-126">Pointeur vers une mémoire tampon qui contient des données de matériaux.</span><span class="sxs-lookup"><span data-stu-id="dea05-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="dea05-127">La mémoire tampon contient un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations du fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="dea05-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="dea05-128">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="dea05-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="dea05-129">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea05-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-130">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dea05-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dea05-131">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="dea05-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="dea05-132">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="dea05-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="dea05-133">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="dea05-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="dea05-134">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="dea05-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="dea05-135">*pNumMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea05-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-136">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dea05-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dea05-137">Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="dea05-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="dea05-138">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dea05-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea05-139">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="dea05-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="dea05-140">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="dea05-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea05-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dea05-141">Return value</span></span>

<span data-ttu-id="dea05-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dea05-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dea05-143">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dea05-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dea05-144">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dea05-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dea05-145">Notes</span><span class="sxs-lookup"><span data-stu-id="dea05-145">Remarks</span></span>

<span data-ttu-id="dea05-146">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="dea05-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="dea05-147">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadMeshFromXW.</span><span class="sxs-lookup"><span data-stu-id="dea05-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="dea05-148">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadMeshFromXA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="dea05-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="dea05-149">Tous les maillages du fichier seront réduits en un seul maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="dea05-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="dea05-150">Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.</span><span class="sxs-lookup"><span data-stu-id="dea05-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="dea05-151">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="dea05-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="dea05-152">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="dea05-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="dea05-153">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="dea05-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="dea05-154">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="dea05-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="dea05-155">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="dea05-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea05-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dea05-156">Requirements</span></span>



| <span data-ttu-id="dea05-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dea05-157">Requirement</span></span> | <span data-ttu-id="dea05-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="dea05-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea05-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="dea05-159">Header</span></span><br/>  | <dl> <span data-ttu-id="dea05-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea05-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dea05-161">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dea05-161">Library</span></span><br/> | <dl> <span data-ttu-id="dea05-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dea05-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dea05-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dea05-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea05-164">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="dea05-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="dea05-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="dea05-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="dea05-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="dea05-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
