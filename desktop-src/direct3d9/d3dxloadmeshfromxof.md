---
description: Charge un maillage à partir d’un objet ID3DXFileData.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: D3DXLoadMeshFromXof, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322897"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="83612-103">D3DXLoadMeshFromXof fonction)</span><span class="sxs-lookup"><span data-stu-id="83612-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="83612-104">Charge un maillage à partir d’un objet [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="83612-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="83612-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83612-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="83612-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83612-107">*pxofMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83612-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-108">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="83612-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="83612-109">Pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="83612-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="83612-110">*Options* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83612-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83612-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83612-112">Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="83612-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="83612-113">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83612-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-114">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="83612-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="83612-115">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="83612-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="83612-116">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83612-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-117">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="83612-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="83612-118">Pointeur vers une mémoire tampon qui contient les données d’contiguïté.</span><span class="sxs-lookup"><span data-stu-id="83612-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="83612-119">Les données d’adjacence contiennent un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="83612-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="83612-120">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="83612-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="83612-121">*ppMaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83612-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-122">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="83612-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="83612-123">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="83612-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="83612-124">Lorsque la méthode est retournée, ce paramètre est rempli avec un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="83612-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="83612-125">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83612-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-126">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="83612-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="83612-127">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="83612-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="83612-128">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="83612-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="83612-129">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="83612-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="83612-130">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="83612-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="83612-131">*pNumMaterials* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83612-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83612-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83612-133">Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="83612-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="83612-134">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83612-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83612-135">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="83612-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="83612-136">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="83612-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83612-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83612-137">Return value</span></span>

<span data-ttu-id="83612-138">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83612-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83612-139">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83612-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83612-140">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="83612-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="83612-141">Notes</span><span class="sxs-lookup"><span data-stu-id="83612-141">Remarks</span></span>

<span data-ttu-id="83612-142">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="83612-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="83612-143">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="83612-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="83612-144">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="83612-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="83612-145">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="83612-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="83612-146">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="83612-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="83612-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83612-147">Requirements</span></span>



| <span data-ttu-id="83612-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83612-148">Requirement</span></span> | <span data-ttu-id="83612-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="83612-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83612-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="83612-150">Header</span></span><br/>  | <dl> <span data-ttu-id="83612-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="83612-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="83612-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83612-152">Library</span></span><br/> | <dl> <span data-ttu-id="83612-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83612-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83612-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83612-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83612-155">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="83612-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="83612-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="83612-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="83612-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="83612-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
