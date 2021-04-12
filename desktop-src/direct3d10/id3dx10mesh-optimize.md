---
description: Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.
ms.assetid: c03e112a-7c9b-4082-9afe-42e1c20b5f4d
title: 'ID3DX10Mesh :: Optimize, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Optimize
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e3c416b28cefe1a3f7fb487567afac4c99057478
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323086"
---
# <a name="id3dx10meshoptimize-method"></a><span data-ttu-id="4d0b2-103">ID3DX10Mesh :: Optimize, méthode</span><span class="sxs-lookup"><span data-stu-id="4d0b2-103">ID3DX10Mesh::Optimize method</span></span>

<span data-ttu-id="4d0b2-104">Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d0b2-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]  UINT        Flags,
  [in]  UINT        *pFaceRemap,
  [out] LPD3D10BLOB *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="4d0b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d0b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d0b2-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4d0b2-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0b2-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d0b2-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d0b2-109">Spécifie le type d’optimisation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="4d0b2-110">Ce paramètre peut être défini sur une combinaison d’un ou plusieurs indicateurs de D3DXMESHOPT et D3DXMESH (à l’exception de D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly et D3DXMESH \_ WRITEONLY).</span><span class="sxs-lookup"><span data-stu-id="4d0b2-110">This parameter can be set to a combination of one or more flags from D3DXMESHOPT and D3DXMESH (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="4d0b2-111">*pFaceRemap* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4d0b2-111">*pFaceRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0b2-112">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d0b2-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4d0b2-113">Tableau de UINTs, un par visage, qui identifie la facette d’origine qui correspond à chaque visage dans le maillage optimisé.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-113">An array of UINTs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="4d0b2-114">Si la valeur fournie pour cet argument est **null**, les données de remappage de visage ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-114">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="4d0b2-115">*ppVertexRemap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4d0b2-115">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d0b2-116">Type : **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="4d0b2-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="4d0b2-117">Adresse d’un pointeur vers une [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), qui contient une valeur DWORD pour chaque vertex qui spécifie la façon dont les nouveaux vertex sont mappés aux anciens vertex.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-117">Address of a pointer to an [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob), which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="4d0b2-118">Ce remappage est utile si vous devez modifier des données externes en fonction du nouveau mappage de vertex.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-118">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d0b2-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4d0b2-119">Return value</span></span>

<span data-ttu-id="4d0b2-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d0b2-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d0b2-121">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4d0b2-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d0b2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4d0b2-122">Remarks</span></span>

<span data-ttu-id="4d0b2-123">Cette méthode génère un nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-123">This method generates a new mesh.</span></span> <span data-ttu-id="4d0b2-124">Avant d’exécuter Optimize, une application doit générer une mémoire tampon de contiguïté en appelant [**ID3DX10Mesh :: GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span><span class="sxs-lookup"><span data-stu-id="4d0b2-124">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DX10Mesh::GenerateAdjacencyAndPointReps**](id3dx10mesh-generateadjacencyandpointreps.md).</span></span> <span data-ttu-id="4d0b2-125">La mémoire tampon d’adjacence contient des données d’contiguïté, telles qu’une liste de bords et les faces adjacentes les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-125">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="4d0b2-126">Cette méthode est très similaire à la méthode [**ID3DX10Mesh :: CloneMesh**](id3dx10mesh-clonemesh.md) , à ceci près qu’elle peut effectuer une optimisation lors de la génération du nouveau clone de la maille.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-126">This method is very similar to the [**ID3DX10Mesh::CloneMesh**](id3dx10mesh-clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="4d0b2-127">Le maillage de sortie hérite de tous les paramètres de création du maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4d0b2-127">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d0b2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d0b2-128">Requirements</span></span>



| <span data-ttu-id="4d0b2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d0b2-129">Requirement</span></span> | <span data-ttu-id="4d0b2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d0b2-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0b2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d0b2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4d0b2-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d0b2-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d0b2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d0b2-133">Library</span></span><br/> | <dl> <span data-ttu-id="4d0b2-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d0b2-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d0b2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d0b2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d0b2-136">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="4d0b2-136">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="4d0b2-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4d0b2-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
