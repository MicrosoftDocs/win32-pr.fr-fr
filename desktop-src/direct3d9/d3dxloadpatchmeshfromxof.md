---
description: Charge un maillage de correctif à partir d’un objet ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: D3DXLoadPatchMeshFromXof, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522350"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="7ca37-103">D3DXLoadPatchMeshFromXof fonction)</span><span class="sxs-lookup"><span data-stu-id="7ca37-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="7ca37-104">Charge un maillage de correctif à partir d’un objet [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca37-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ca37-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="7ca37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ca37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca37-107">*pxofMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-108">Type : **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="7ca37-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="7ca37-109">Pointeur vers une interface [**ID3DXFileData**](id3dxfiledata.md) , représentant l’objet de données de fichier à charger.</span><span class="sxs-lookup"><span data-stu-id="7ca37-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-110">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ca37-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ca37-112">Combinaison d’un ou de plusieurs indicateurs [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="7ca37-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-113">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-114">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7ca37-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7ca37-115">Pointeur vers l’appareil à partir duquel le maillage est créé.</span><span class="sxs-lookup"><span data-stu-id="7ca37-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-116">*ppMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-117">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ca37-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ca37-118">Tableau de matières contenues dans la maille.</span><span class="sxs-lookup"><span data-stu-id="7ca37-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="7ca37-119">Chaque matériau est indexé par une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca37-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-120">*ppEffectInstances* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-121">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ca37-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ca37-122">Pointeur vers une mémoire tampon qui contient un tableau d’instances d’effet, une par groupe d’attributs dans le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="7ca37-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="7ca37-123">Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet.</span><span class="sxs-lookup"><span data-stu-id="7ca37-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="7ca37-124">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="7ca37-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="7ca37-125">Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7ca37-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-126">*pNumMaterials* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-127">Type : **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="7ca37-127">Type: **PDWORD**</span></span>

<span data-ttu-id="7ca37-128">Pointeur qui contient le nombre de matériaux dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="7ca37-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7ca37-129">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7ca37-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ca37-130">Type : **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ca37-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="7ca37-131">Adresse d’un pointeur vers une interface [**ID3DXPatchMesh**](id3dxpatchmesh.md) représentant le maillage chargé.</span><span class="sxs-lookup"><span data-stu-id="7ca37-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca37-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ca37-132">Return value</span></span>

<span data-ttu-id="7ca37-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ca37-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ca37-134">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7ca37-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ca37-135">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7ca37-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca37-136">Notes</span><span class="sxs-lookup"><span data-stu-id="7ca37-136">Remarks</span></span>

<span data-ttu-id="7ca37-137">Pour les fichiers de maillage qui ne contiennent pas d’informations sur l’instance d’effet, les instances d’effet par défaut sont générées à partir des informations matérielles du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="7ca37-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="7ca37-138">Une instance d’effet par défaut aura des valeurs par défaut qui correspondent aux membres de la structure [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca37-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="7ca37-139">Le nom de texture par défaut est également renseigné, mais est géré différemment.</span><span class="sxs-lookup"><span data-stu-id="7ca37-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="7ca37-140">Le nom est Texture0@Name , ce qui correspond à une variable Effect par le nom de « Texture0 » avec une annotation appelée « Name ».</span><span class="sxs-lookup"><span data-stu-id="7ca37-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="7ca37-141">Contient le nom de fichier de chaîne pour la texture.</span><span class="sxs-lookup"><span data-stu-id="7ca37-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca37-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ca37-142">Requirements</span></span>



| <span data-ttu-id="7ca37-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ca37-143">Requirement</span></span> | <span data-ttu-id="7ca37-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ca37-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca37-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ca37-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7ca37-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ca37-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7ca37-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7ca37-147">Library</span></span><br/> | <dl> <span data-ttu-id="7ca37-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ca37-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ca37-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ca37-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca37-150">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="7ca37-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7ca37-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7ca37-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="7ca37-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="7ca37-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
