---
description: Effectuez des dépassements de logiciels sur un tableau de vertex.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: ID3DX10SkinInfo ::D méthode oSoftwareSkinning (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535178"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a><span data-ttu-id="08b46-103">ID3DX10SkinInfo ::D méthode oSoftwareSkinning</span><span class="sxs-lookup"><span data-stu-id="08b46-103">ID3DX10SkinInfo::DoSoftwareSkinning method</span></span>

<span data-ttu-id="08b46-104">Effectuez des dépassements de logiciels sur un tableau de vertex.</span><span class="sxs-lookup"><span data-stu-id="08b46-104">Do software skinning on an array of vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08b46-105">Syntax</span></span>


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a><span data-ttu-id="08b46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08b46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b46-107">*StartVertex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-107">*StartVertex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08b46-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08b46-109">Index de base 0 dans pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="08b46-109">A 0-based index into pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-110">*VertexCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-110">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08b46-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08b46-112">Nombre de vertex à transformer.</span><span class="sxs-lookup"><span data-stu-id="08b46-112">Number of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-113">*pSrcVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-113">*pSrcVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-114">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="08b46-114">Type: **void\***</span></span>

<span data-ttu-id="08b46-115">Pointeur vers un tableau de vertex à transformer.</span><span class="sxs-lookup"><span data-stu-id="08b46-115">Pointer to an array of vertices to transform.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-116">*SrcStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-116">*SrcStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08b46-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08b46-118">Taille, en octets, d’un vertex dans pSrcVertices.</span><span class="sxs-lookup"><span data-stu-id="08b46-118">The size, in bytes, of a vertex in pSrcVertices.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-119">*pDestVertices* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08b46-119">*pDestVertices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-120">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="08b46-120">Type: **void\***</span></span>

<span data-ttu-id="08b46-121">Pointeur vers un tableau de vertex, qui sera rempli avec les vertex transformés.</span><span class="sxs-lookup"><span data-stu-id="08b46-121">Pointer to an array of vertices, which will be filled with the transformed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-122">*DestStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-122">*DestStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08b46-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08b46-124">Taille, en octets, d’un vertex dans pDestVertices.</span><span class="sxs-lookup"><span data-stu-id="08b46-124">The size, in bytes, of a vertex in pDestVertices.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-125">*pBoneMatrices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-125">*pBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-126">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="08b46-126">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="08b46-127">Tableau de matrices qui sera utilisé pour transformer les points mappés à chaque segment, de telle sorte que les vertex mappés au segment \[ \] sont transformés par pBoneMatrices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="08b46-127">An array of matrices that will be used to transform the points mapped to each bone, such that the vertices mapped to bone\[i\] will be transformed by pBoneMatrices\[i\].</span></span> <span data-ttu-id="08b46-128">Ce tableau sera utilisé pour transformer les matrices uniquement si la valeur IsNormal dans pChannelDescs est définie sur **false**, sinon pInverseTransposeBoneMatrices sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="08b46-128">This array will be used to transform the matrices only if the IsNormal value in pChannelDescs is set to **FALSE**, otherwise pInverseTransposeBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-129">*pInverseTransposeBoneMatrices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-129">*pInverseTransposeBoneMatrices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-130">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="08b46-130">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="08b46-131">Si cette valeur est **null**, elle sera définie sur pBoneMatrices.</span><span class="sxs-lookup"><span data-stu-id="08b46-131">If this value is **NULL**, it will be set equal to pBoneMatrices.</span></span> <span data-ttu-id="08b46-132">Ce tableau de matrices sera utilisé pour transformer les vertex uniquement si la valeur IsNormal dans pChannelDescs est définie sur **true**, sinon pBoneMatrices sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="08b46-132">This array of matrices will be used to transform the vertices only if the IsNormal value in pChannelDescs is set to **TRUE**, otherwise pBoneMatrices will be used.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-133">*pChannelDescs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-133">*pChannelDescs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-134">Type : d3dx10 de l' **[ **\_ apparence du \_ canal**](d3dx10-skinning-channel.md)\***</span><span class="sxs-lookup"><span data-stu-id="08b46-134">Type: **[**D3DX10\_SKINNING\_CHANNEL**](d3dx10-skinning-channel.md)\***</span></span>

<span data-ttu-id="08b46-135">Pointeur vers une \_ structure de canal d’apparence d3dx10 \_ , qui détermine le membre du vertex decl sur lequel le détourage de logiciel sera effectué.</span><span class="sxs-lookup"><span data-stu-id="08b46-135">Pointer to a D3DX10\_SKINNING\_CHANNEL structure, which determines the member of the vertex decl the software skinning will be done on.</span></span>

</dd> <dt>

<span data-ttu-id="08b46-136">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="08b46-136">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b46-137">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08b46-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08b46-138">Nombre de structures de \_ canal d’apparence d3dx10 \_ dans pChannelDescs.</span><span class="sxs-lookup"><span data-stu-id="08b46-138">The number of D3DX10\_SKINNING\_CHANNEL structures in pChannelDescs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b46-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08b46-139">Return value</span></span>

<span data-ttu-id="08b46-140">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08b46-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08b46-141">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08b46-141">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="08b46-142">Si la méthode échoue, la valeur de retour peut être : E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="08b46-142">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="08b46-143">Notes</span><span class="sxs-lookup"><span data-stu-id="08b46-143">Remarks</span></span>

<span data-ttu-id="08b46-144">Voici un exemple d’utilisation de l’application de pelures de logiciels :</span><span class="sxs-lookup"><span data-stu-id="08b46-144">Here is an example of how to use software skinning:</span></span>


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a><span data-ttu-id="08b46-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08b46-145">Requirements</span></span>



| <span data-ttu-id="08b46-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08b46-146">Requirement</span></span> | <span data-ttu-id="08b46-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="08b46-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08b46-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="08b46-148">Header</span></span><br/>  | <dl> <span data-ttu-id="08b46-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b46-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="08b46-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08b46-150">Library</span></span><br/> | <dl> <span data-ttu-id="08b46-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08b46-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b46-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08b46-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b46-153">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="08b46-153">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="08b46-154">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="08b46-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
