---
description: Convertissez le sous-ensemble de maillage spécifié en une série de bandes.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: D3DXConvertMeshSubsetToStrips, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522986"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="d8420-103">D3DXConvertMeshSubsetToStrips fonction)</span><span class="sxs-lookup"><span data-stu-id="d8420-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="d8420-104">Convertissez le sous-ensemble de maillage spécifié en une série de bandes.</span><span class="sxs-lookup"><span data-stu-id="d8420-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8420-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8420-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="d8420-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8420-107">*Mailler* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8420-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-108">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="d8420-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="d8420-109">Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à convertir en bande.</span><span class="sxs-lookup"><span data-stu-id="d8420-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-110">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8420-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8420-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8420-112">ID d’attribut du sous-ensemble de maillage à convertir en bandes.</span><span class="sxs-lookup"><span data-stu-id="d8420-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-113">*IBOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8420-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8420-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8420-115">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options pour la création de la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="d8420-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="d8420-116">Ne peut pas être D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8420-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="d8420-117">Le tampon d’index sera créé avec des index 32 bits ou 16 bits selon le format de la mémoire tampon d’index de la maille spécifiée par le paramètre *meshy* .</span><span class="sxs-lookup"><span data-stu-id="d8420-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-118">*ppIndexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8420-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-119">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="d8420-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="d8420-120">Pointeur vers une interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , représentant la mémoire tampon d’index contenant la bande.</span><span class="sxs-lookup"><span data-stu-id="d8420-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-121">*pNumIndices* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8420-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8420-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8420-123">Nombre d’index dans la mémoire tampon retournée dans le paramètre *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="d8420-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-124">*ppStripLengths* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8420-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-125">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8420-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d8420-126">Mémoire tampon contenant un tableau d’un DWORD par bande, qui spécifie le nombre de triangles dans cette frange.</span><span class="sxs-lookup"><span data-stu-id="d8420-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="d8420-127">*pNumStrips* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d8420-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8420-128">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8420-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8420-129">Nombre de bandes individuelles dans le tampon d’index et le tableau de longueur de bande correspondant.</span><span class="sxs-lookup"><span data-stu-id="d8420-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8420-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8420-130">Return value</span></span>

<span data-ttu-id="d8420-131">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8420-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8420-132">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8420-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8420-133">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d8420-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8420-134">Notes</span><span class="sxs-lookup"><span data-stu-id="d8420-134">Remarks</span></span>

<span data-ttu-id="d8420-135">Avant d’exécuter cette fonction, appelez [**optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), avec l' \_ indicateur D3DXMESHOPT ATTRSORT défini.</span><span class="sxs-lookup"><span data-stu-id="d8420-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8420-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8420-136">Requirements</span></span>



| <span data-ttu-id="d8420-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8420-137">Requirement</span></span> | <span data-ttu-id="d8420-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8420-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8420-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8420-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d8420-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8420-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d8420-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d8420-141">Library</span></span><br/> | <dl> <span data-ttu-id="d8420-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8420-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8420-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8420-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8420-144">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="d8420-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
