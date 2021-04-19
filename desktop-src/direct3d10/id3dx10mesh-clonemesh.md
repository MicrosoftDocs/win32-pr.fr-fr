---
description: Crée un nouveau maillage et le remplit avec les données d’un maillage précédemment chargé.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh :: CloneMesh, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531353"
---
# <a name="id3dx10meshclonemesh-method"></a><span data-ttu-id="cc985-103">ID3DX10Mesh :: CloneMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="cc985-103">ID3DX10Mesh::CloneMesh method</span></span>

<span data-ttu-id="cc985-104">Crée un nouveau maillage et le remplit avec les données d’un maillage précédemment chargé.</span><span class="sxs-lookup"><span data-stu-id="cc985-104">Creates a new mesh and fills it with the data of a previously loaded mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc985-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc985-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="cc985-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc985-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc985-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="cc985-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc985-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc985-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc985-109">Indicateurs de création à appliquer au nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="cc985-109">Creation flags to be applied to the new mesh.</span></span> <span data-ttu-id="cc985-110">Consultez [**d3dx10 \_ Mesh**](d3dx10-mesh.md).</span><span class="sxs-lookup"><span data-stu-id="cc985-110">See [**D3DX10\_MESH**](d3dx10-mesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc985-111">*pPosSemantic* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc985-111">*pPosSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc985-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc985-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc985-113">Nom sémantique pour les données de position.</span><span class="sxs-lookup"><span data-stu-id="cc985-113">The semantic name for the position data.</span></span>

</dd> <dt>

<span data-ttu-id="cc985-114">*pDesc* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc985-114">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc985-115">Type : **const [**D3D10 \_ élément d’entrée \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cc985-115">Type: **const [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)\***</span></span>

<span data-ttu-id="cc985-116">Tableau des \_ structures DESC d’élément d’entrée D3D10 \_ \_ , décrivant le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="cc985-116">Array of D3D10\_INPUT\_ELEMENT\_DESC structures, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="cc985-117">Consultez [**Description de l' \_ \_ élément \_ d’entrée D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="cc985-117">See [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).</span></span>

</dd> <dt>

<span data-ttu-id="cc985-118">*DeclCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc985-118">*DeclCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc985-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc985-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc985-120">Nombre d’éléments dans le tableau pDesc.</span><span class="sxs-lookup"><span data-stu-id="cc985-120">The number of elements in the pDesc array.</span></span>

</dd> <dt>

<span data-ttu-id="cc985-121">*ppCloneMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc985-121">*ppCloneMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc985-122">Type : **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc985-122">Type: **[**ID3DX10Mesh**](id3dx10mesh.md)\*\***</span></span>

<span data-ttu-id="cc985-123">Nouveau maillage.</span><span class="sxs-lookup"><span data-stu-id="cc985-123">The new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc985-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc985-124">Return value</span></span>

<span data-ttu-id="cc985-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc985-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc985-126">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cc985-126">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc985-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc985-127">Requirements</span></span>



| <span data-ttu-id="cc985-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc985-128">Requirement</span></span> | <span data-ttu-id="cc985-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc985-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc985-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc985-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cc985-131"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc985-131"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc985-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cc985-132">Library</span></span><br/> | <dl> <span data-ttu-id="cc985-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc985-133"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc985-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc985-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc985-135">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cc985-135">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cc985-136">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cc985-136">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
