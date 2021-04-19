---
description: Génère un maillage simplifié à l’aide des poids fournis qui sont disponibles le plus près possible de l’MinValue donné.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: D3DXSimplifyMesh, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523821"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="732bb-103">D3DXSimplifyMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="732bb-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="732bb-104">Génère un maillage simplifié à l’aide des poids fournis qui sont disponibles le plus près possible de l’MinValue donné.</span><span class="sxs-lookup"><span data-stu-id="732bb-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="732bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="732bb-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="732bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="732bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732bb-107">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="732bb-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="732bb-109">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant la maille source.</span><span class="sxs-lookup"><span data-stu-id="732bb-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-110">*pAdjacency* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-111">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="732bb-112">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage de la maille à simplifier.</span><span class="sxs-lookup"><span data-stu-id="732bb-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-113">*pVertexAttributeWeights* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-114">Type : **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="732bb-115">Pointeur vers une structure [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , contenant le poids de chaque composant de vertex.</span><span class="sxs-lookup"><span data-stu-id="732bb-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="732bb-116">Si ce paramètre a la valeur **null**, une structure par défaut est utilisée.</span><span class="sxs-lookup"><span data-stu-id="732bb-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="732bb-117">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="732bb-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-118">*pVertexWeights* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-119">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="732bb-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="732bb-120">Pointeur vers un tableau de poids de vertex.</span><span class="sxs-lookup"><span data-stu-id="732bb-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="732bb-121">Si ce paramètre a la valeur **null**, tous les poids des vertex ont la valeur 1,0.</span><span class="sxs-lookup"><span data-stu-id="732bb-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-122">*MinValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="732bb-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="732bb-124">Nombre de vertex ou de faces, selon l’indicateur défini dans le paramètre *options* , par lequel simplifier le maillage source.</span><span class="sxs-lookup"><span data-stu-id="732bb-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-125">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="732bb-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-126">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="732bb-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="732bb-127">Spécifie les options de simplification de la maille.</span><span class="sxs-lookup"><span data-stu-id="732bb-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="732bb-128">L’un des indicateurs dans [**D3DXMESHSIMP**](./d3dxmeshsimp.md) peut être défini.</span><span class="sxs-lookup"><span data-stu-id="732bb-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="732bb-129">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="732bb-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="732bb-130">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="732bb-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="732bb-131">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage de simplification retourné.</span><span class="sxs-lookup"><span data-stu-id="732bb-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="732bb-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="732bb-132">Return value</span></span>

<span data-ttu-id="732bb-133">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="732bb-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="732bb-134">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="732bb-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="732bb-135">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="732bb-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="732bb-136">Notes</span><span class="sxs-lookup"><span data-stu-id="732bb-136">Remarks</span></span>

<span data-ttu-id="732bb-137">Cette fonction génère un maillage qui a des vertex ou des visages *MinValue* .</span><span class="sxs-lookup"><span data-stu-id="732bb-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="732bb-138">Si le processus de simplification ne peut pas réduire le maillage à *MinValue*, l’appel s’effectue toujours car *MinValue* est un minimum souhaité, et non un minimum absolu.</span><span class="sxs-lookup"><span data-stu-id="732bb-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="732bb-139">Si *pVertexAttributeWeights* a la valeur **null**, les valeurs suivantes sont affectées à la structure [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) par défaut.</span><span class="sxs-lookup"><span data-stu-id="732bb-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="732bb-140">Il s’agit de la structure par défaut que la plupart des applications doivent utiliser, car elle ne prend en compte que le réglage géométrique et normal.</span><span class="sxs-lookup"><span data-stu-id="732bb-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="732bb-141">Dans certains cas particuliers, les autres champs de membre doivent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="732bb-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="732bb-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="732bb-142">Requirements</span></span>



| <span data-ttu-id="732bb-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="732bb-143">Requirement</span></span> | <span data-ttu-id="732bb-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="732bb-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="732bb-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="732bb-145">Header</span></span><br/>  | <dl> <span data-ttu-id="732bb-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="732bb-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="732bb-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="732bb-147">Library</span></span><br/> | <dl> <span data-ttu-id="732bb-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="732bb-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="732bb-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="732bb-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="732bb-150">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="732bb-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
