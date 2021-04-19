---
description: Demande l’allocation d’un objet conteneur de maillage.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy :: CreateMeshContainer, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531518"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="098b0-103">ID3DXAllocateHierarchy :: CreateMeshContainer, méthode</span><span class="sxs-lookup"><span data-stu-id="098b0-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="098b0-104">Demande l’allocation d’un objet conteneur de maillage.</span><span class="sxs-lookup"><span data-stu-id="098b0-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="098b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="098b0-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="098b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="098b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098b0-107">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="098b0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="098b0-109">Nom de la maille.</span><span class="sxs-lookup"><span data-stu-id="098b0-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="098b0-110">*pMeshData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-111">Type : **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="098b0-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="098b0-112">Pointeur vers la structure de données de maillage.</span><span class="sxs-lookup"><span data-stu-id="098b0-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="098b0-113">Consultez [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="098b0-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="098b0-114">*pMaterials* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-115">Type : **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="098b0-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="098b0-116">Tableau de matériaux utilisés dans la maille.</span><span class="sxs-lookup"><span data-stu-id="098b0-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="098b0-117">*pEffectInstances* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-118">Type : **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="098b0-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="098b0-119">Tableau d’instances d’effet utilisé dans la maille.</span><span class="sxs-lookup"><span data-stu-id="098b0-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="098b0-120">Consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="098b0-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="098b0-121">*NumMaterials* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="098b0-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="098b0-123">Nombre de matériaux dans le tableau de matériaux.</span><span class="sxs-lookup"><span data-stu-id="098b0-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="098b0-124">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-125">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="098b0-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="098b0-126">Tableau d’adjacence pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="098b0-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="098b0-127">*pSkinInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="098b0-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-128">Type : **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="098b0-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="098b0-129">Pointeur vers l’objet de maillage d’apparence si des données d’apparence sont trouvées.</span><span class="sxs-lookup"><span data-stu-id="098b0-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="098b0-130">Consultez [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="098b0-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="098b0-131">*ppNewMeshContainer* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="098b0-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="098b0-132">Type : **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="098b0-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="098b0-133">Retourne le conteneur de maillage créé.</span><span class="sxs-lookup"><span data-stu-id="098b0-133">Returns the created mesh container.</span></span> <span data-ttu-id="098b0-134">Consultez [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="098b0-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098b0-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="098b0-135">Return value</span></span>

<span data-ttu-id="098b0-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="098b0-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="098b0-137">Les valeurs de retour de cette méthode sont implémentées par un programmeur d’applications.</span><span class="sxs-lookup"><span data-stu-id="098b0-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="098b0-138">En général, si aucune erreur ne se produit, programmez la méthode pour retourner D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="098b0-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="098b0-139">Sinon, programmez la méthode pour retourner un message d’erreur approprié à partir de D3DERR ou D3DXERR, car cela entraînera l’échec de [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) également et retourne l’erreur.</span><span class="sxs-lookup"><span data-stu-id="098b0-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="098b0-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="098b0-140">Requirements</span></span>



| <span data-ttu-id="098b0-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="098b0-141">Requirement</span></span> | <span data-ttu-id="098b0-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="098b0-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="098b0-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="098b0-143">Header</span></span><br/>  | <dl> <span data-ttu-id="098b0-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="098b0-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="098b0-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="098b0-145">Library</span></span><br/> | <dl> <span data-ttu-id="098b0-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="098b0-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="098b0-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="098b0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098b0-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="098b0-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
