---
description: Charge un maillage d’apparence à partir d’un objet de données de fichier DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: D3DXLoadSkinMeshFromXof, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761948"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="1168e-103">D3DXLoadSkinMeshFromXof fonction)</span><span class="sxs-lookup"><span data-stu-id="1168e-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="1168e-104">Charge un maillage d’apparence à partir d’un objet de données de fichier DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="1168e-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1168e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1168e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1168e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1168e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1168e-107">*pxofMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1168e-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-108">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="1168e-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="1168e-109">Pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="1168e-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-110">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1168e-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1168e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1168e-112">Combinaison d’un ou plusieurs indicateurs à partir de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options de création pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="1168e-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-113">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1168e-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-114">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1168e-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1168e-115">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.</span><span class="sxs-lookup"><span data-stu-id="1168e-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-116">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-117">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1168e-118">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1168e-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1168e-119">Lorsque cette méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="1168e-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-120">*ppMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-121">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1168e-122">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1168e-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1168e-123">Lorsque la méthode est retournée, ce paramètre est rempli avec un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="1168e-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-124">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1168e-126">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="1168e-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="1168e-127">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="1168e-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="1168e-128">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="1168e-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="1168e-129">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1168e-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="1168e-130">*pMatOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1168e-132">Pointeur vers le nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *ppMaterials* , lorsque la méthode retourne.</span><span class="sxs-lookup"><span data-stu-id="1168e-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-133">*ppSkinInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-134">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="1168e-135">Adresse d’un pointeur vers une interface [**ID3DXSkinInfo**](id3dxskininfo.md) , qui représente les informations d’apparence.</span><span class="sxs-lookup"><span data-stu-id="1168e-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="1168e-136">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1168e-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1168e-137">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1168e-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1168e-138">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , qui représente le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="1168e-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1168e-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1168e-139">Return value</span></span>

<span data-ttu-id="1168e-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1168e-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1168e-141">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1168e-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1168e-142">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1168e-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="1168e-143">Notes</span><span class="sxs-lookup"><span data-stu-id="1168e-143">Remarks</span></span>

<span data-ttu-id="1168e-144">Cette méthode prend un pointeur vers un objet interne dans le fichier. x, ce qui vous permet de charger la hiérarchie des frames.</span><span class="sxs-lookup"><span data-stu-id="1168e-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="1168e-145">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="1168e-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="1168e-146">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="1168e-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="1168e-147">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="1168e-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="1168e-148">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="1168e-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="1168e-149">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="1168e-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="1168e-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1168e-150">Requirements</span></span>



| <span data-ttu-id="1168e-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1168e-151">Requirement</span></span> | <span data-ttu-id="1168e-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="1168e-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1168e-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="1168e-153">Header</span></span><br/>  | <dl> <span data-ttu-id="1168e-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1168e-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1168e-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1168e-155">Library</span></span><br/> | <dl> <span data-ttu-id="1168e-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1168e-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1168e-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1168e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1168e-158">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="1168e-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1168e-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1168e-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="1168e-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="1168e-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
