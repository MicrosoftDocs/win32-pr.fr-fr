---
description: Calcule les IMT par triangle à partir des données par vertex. Cette fonction vous permet de calculer le IMT en fonction de la valeur d’une maille (couleur, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: D3DXComputeIMTFromPerVertexSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538061"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a><span data-ttu-id="ce129-104">D3DXComputeIMTFromPerVertexSignal fonction)</span><span class="sxs-lookup"><span data-stu-id="ce129-104">D3DXComputeIMTFromPerVertexSignal function</span></span>

<span data-ttu-id="ce129-105">Calcule les IMT par triangle à partir des données par vertex.</span><span class="sxs-lookup"><span data-stu-id="ce129-105">Calculate per-triangle IMT's from from per-vertex data.</span></span> <span data-ttu-id="ce129-106">Cette fonction vous permet de calculer le IMT en fonction de la valeur d’une maille (couleur, normal, etc.).</span><span class="sxs-lookup"><span data-stu-id="ce129-106">This function allows you to calculate the IMT based off of any value in a mesh (color, normal, etc).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce129-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce129-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="ce129-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce129-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce129-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="ce129-111">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.</span><span class="sxs-lookup"><span data-stu-id="ce129-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-112">*pfVertexSignal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-112">*pfVertexSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-113">Type : **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ce129-113">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ce129-114">Pointeur vers un tableau de données par vertex à partir duquel IMT sera calculé.</span><span class="sxs-lookup"><span data-stu-id="ce129-114">A pointer to an array of per-vertex data from which IMT will be computed.</span></span> <span data-ttu-id="ce129-115">La taille du tableau est uSignalStride \* v, où v est le nombre de vertex dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="ce129-115">The array size is uSignalStride \* v, where v is the number of vertices in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-116">*uSignalDimension* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-116">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce129-118">Nombre de valeurs float par vertex.</span><span class="sxs-lookup"><span data-stu-id="ce129-118">The number of floats per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-119">*uSignalStride* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-119">*uSignalStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce129-121">Nombre d’octets par vertex dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ce129-121">The number of bytes per vertex in the array.</span></span> <span data-ttu-id="ce129-122">Il doit s’agir d’un multiple de sizeof (float)</span><span class="sxs-lookup"><span data-stu-id="ce129-122">This must be a multiple of sizeof(float)</span></span>

</dd> <dt>

<span data-ttu-id="ce129-123">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-123">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-124">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce129-125">Options de retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="ce129-125">Texture wrap options.</span></span> <span data-ttu-id="ce129-126">Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ce129-126">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce129-127">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="ce129-127">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="ce129-128">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-128">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="ce129-129">Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.</span><span class="sxs-lookup"><span data-stu-id="ce129-129">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-130">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="ce129-130">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="ce129-131">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce129-131">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce129-132">Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="ce129-132">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="ce129-133">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="ce129-133">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-134">*ppIMTData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ce129-134">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-135">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce129-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ce129-136">Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné.</span><span class="sxs-lookup"><span data-stu-id="ce129-136">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="ce129-137">Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.</span><span class="sxs-lookup"><span data-stu-id="ce129-137">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce129-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce129-138">Return value</span></span>

<span data-ttu-id="ce129-139">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce129-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce129-140">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ce129-140">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce129-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce129-141">Requirements</span></span>



| <span data-ttu-id="ce129-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce129-142">Requirement</span></span> | <span data-ttu-id="ce129-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce129-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce129-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce129-144">Header</span></span><br/>  | <dl> <span data-ttu-id="ce129-145"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ce129-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce129-146">Library</span></span><br/> | <dl> <span data-ttu-id="ce129-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce129-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce129-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce129-149">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="ce129-149">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="ce129-150">Utilisation de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ce129-150">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
