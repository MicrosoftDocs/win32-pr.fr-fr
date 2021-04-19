---
description: Convertit le sous-ensemble de maillage spécifié en une seule bande triangulaire.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539163"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="5f0c8-103">D3DXConvertMeshSubsetToSingleStrip fonction)</span><span class="sxs-lookup"><span data-stu-id="5f0c8-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="5f0c8-104">Convertit le sous-ensemble de maillage spécifié en une seule bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f0c8-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="5f0c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f0c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0c8-107">*Mailler* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f0c8-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0c8-108">Type : **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0c8-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="5f0c8-109">Pointeur vers une interface [**ID3DXBaseMesh**](id3dxbasemesh.md) représentant le maillage à convertir en bande.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="5f0c8-110">*AttribId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f0c8-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0c8-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0c8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f0c8-112">ID d’attribut du sous-ensemble de maillage à convertir en bandes.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="5f0c8-113">*IBOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f0c8-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0c8-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0c8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5f0c8-115">Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant des options pour la création de la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="5f0c8-116">Ne peut pas être D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="5f0c8-117">Le tampon d’index sera créé avec des index 32 bits ou 16 bits, selon le format de la mémoire tampon d’index de la maille spécifiée par le paramètre *meshy* .</span><span class="sxs-lookup"><span data-stu-id="5f0c8-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5f0c8-118">*ppIndexBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f0c8-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0c8-119">Type : **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="5f0c8-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="5f0c8-120">Pointeur vers une interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , représentant la mémoire tampon d’index contenant la bande.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="5f0c8-121">*pNumIndices* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5f0c8-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0c8-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f0c8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5f0c8-123">Nombre d’index dans la mémoire tampon retournée dans le paramètre *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="5f0c8-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0c8-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f0c8-124">Return value</span></span>

<span data-ttu-id="5f0c8-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5f0c8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5f0c8-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5f0c8-127">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f0c8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5f0c8-128">Remarks</span></span>

<span data-ttu-id="5f0c8-129">Avant d’exécuter cette fonction, appelez [**optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), avec l' \_ indicateur D3DXMESHOPT ATTRSORT défini.</span><span class="sxs-lookup"><span data-stu-id="5f0c8-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0c8-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f0c8-130">Requirements</span></span>



| <span data-ttu-id="5f0c8-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f0c8-131">Requirement</span></span> | <span data-ttu-id="5f0c8-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f0c8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0c8-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f0c8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5f0c8-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0c8-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5f0c8-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5f0c8-135">Library</span></span><br/> | <dl> <span data-ttu-id="5f0c8-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f0c8-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f0c8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f0c8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0c8-138">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="5f0c8-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
