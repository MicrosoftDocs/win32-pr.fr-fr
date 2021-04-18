---
description: Sous-divise les visages sur une maille, ce qui permet un échantillonnage adaptatif prudent qui n’élimine pas les caractéristiques de la maille.
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine :: RobustMeshRefine, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522614"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="09f40-103">ID3DXPRTEngine :: RobustMeshRefine, méthode</span><span class="sxs-lookup"><span data-stu-id="09f40-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="09f40-104">Sous-divise les visages sur une maille, ce qui permet un échantillonnage adaptatif prudent qui n’élimine pas les caractéristiques de la maille.</span><span class="sxs-lookup"><span data-stu-id="09f40-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09f40-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="09f40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09f40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f40-107">*MinEdgeLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09f40-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f40-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09f40-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09f40-109">Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="09f40-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="09f40-110">Si la valeur est zéro, une valeur par défaut raisonnable est remplacée.</span><span class="sxs-lookup"><span data-stu-id="09f40-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="09f40-111">*MaxSubdiv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09f40-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f40-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09f40-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09f40-113">Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif.</span><span class="sxs-lookup"><span data-stu-id="09f40-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="09f40-114">Si la valeur est zéro, la valeur par défaut 5 est remplacée.</span><span class="sxs-lookup"><span data-stu-id="09f40-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f40-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09f40-115">Return value</span></span>

<span data-ttu-id="09f40-116">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09f40-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09f40-117">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09f40-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="09f40-118">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="09f40-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f40-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09f40-119">Requirements</span></span>



| <span data-ttu-id="09f40-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09f40-120">Requirement</span></span> | <span data-ttu-id="09f40-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="09f40-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="09f40-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="09f40-122">Header</span></span><br/>  | <dl> <span data-ttu-id="09f40-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f40-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="09f40-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09f40-124">Library</span></span><br/> | <dl> <span data-ttu-id="09f40-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09f40-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="09f40-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09f40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f40-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="09f40-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="09f40-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span><span class="sxs-lookup"><span data-stu-id="09f40-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="09f40-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span><span class="sxs-lookup"><span data-stu-id="09f40-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
