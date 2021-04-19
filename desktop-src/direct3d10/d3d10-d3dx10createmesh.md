---
description: Crée un objet de maillage à l’aide d’un déclarateur.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: D3DX10CreateMesh, fonction (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535198"
---
# <a name="d3dx10createmesh-function"></a><span data-ttu-id="1ca3b-103">D3DX10CreateMesh fonction)</span><span class="sxs-lookup"><span data-stu-id="1ca3b-103">D3DX10CreateMesh function</span></span>

<span data-ttu-id="1ca3b-104">Crée un objet de maillage à l’aide d’un déclarateur.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ca3b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1ca3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ca3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca3b-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-108">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1ca3b-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1ca3b-109">Pointeur vers une [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), l’objet appareil à associer à la maille.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-109">Pointer to an [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-110">*pDeclaration* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-111">Type : **const [**D3D10 \_ élément d’entrée \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="1ca3b-111">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="1ca3b-112">Tableau d’éléments de [**\_ \_ \_ Description d’élément d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , décrivant le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-112">Array of [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="1ca3b-113">Ce paramètre doit être directement mappé à un format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-113">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-114">*DeclCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-114">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca3b-116">Nombre d’éléments dans pDeclaration.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-116">The number of elements in pDeclaration.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-117">*pPositionSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-117">*pPositionSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-118">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca3b-119">Sémantique qui identifie la partie de la déclaration de vertex qui contient des informations de position.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-119">Semantic that identifies which part of the vertex declaration contains position information.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-120">*VertexCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-120">*VertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-121">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca3b-122">Nombre de vertex pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-122">Number of vertices for the mesh.</span></span> <span data-ttu-id="1ca3b-123">Ce paramètre doit être supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-123">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-124">*FaceCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-124">*FaceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-125">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca3b-126">Nombre de faces de la maille.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-126">Number of faces for the mesh.</span></span> <span data-ttu-id="1ca3b-127">La plage valide pour ce nombre est supérieure à 0, et une valeur inférieure à la valeur DWORD maximale (généralement 65534), car le dernier index est réservé.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-127">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-128">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-128">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-129">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ca3b-130">Combinaison d’un ou plusieurs indicateurs à partir de la [**\_ maille d3dx10**](d3dx10-mesh.md), en spécifiant des options pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-130">Combination of one or more flags from the [**D3DX10\_MESH**](d3dx10-mesh.md), specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1ca3b-131">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1ca3b-131">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca3b-132">Type : **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ca3b-132">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="1ca3b-133">Adresse d’un pointeur vers une [**interface ID3DX10Mesh**](id3dx10mesh.md)représentant l’objet de maillage créé.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-133">Address of a pointer to an [**ID3DX10Mesh Interface**](id3dx10mesh.md), representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca3b-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ca3b-134">Return value</span></span>

<span data-ttu-id="1ca3b-135">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ca3b-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ca3b-136">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ca3b-137">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1ca3b-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca3b-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ca3b-138">Requirements</span></span>



| <span data-ttu-id="1ca3b-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ca3b-139">Requirement</span></span> | <span data-ttu-id="1ca3b-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ca3b-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca3b-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ca3b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="1ca3b-142"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca3b-142"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1ca3b-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ca3b-143">Library</span></span><br/> | <dl> <span data-ttu-id="1ca3b-144"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ca3b-144"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ca3b-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ca3b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca3b-146">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="1ca3b-146">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1ca3b-147">D3DX, fonctions</span><span class="sxs-lookup"><span data-stu-id="1ca3b-147">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 
