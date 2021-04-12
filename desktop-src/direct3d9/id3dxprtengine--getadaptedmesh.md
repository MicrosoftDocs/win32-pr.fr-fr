---
description: Retourne un maillage avec les modifications résultant de l’échantillonnage spatial adaptatif. Le maillage retourné contient uniquement des positions, des normales et des coordonnées de texture (s’il est défini).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine :: GetAdaptedMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323254"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="a1982-104">ID3DXPRTEngine :: GetAdaptedMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="a1982-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="a1982-105">Retourne un maillage avec les modifications résultant de l’échantillonnage spatial adaptatif.</span><span class="sxs-lookup"><span data-stu-id="a1982-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="a1982-106">Le maillage retourné contient uniquement des positions, des normales et des coordonnées de texture (s’il est défini).</span><span class="sxs-lookup"><span data-stu-id="a1982-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1982-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1982-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a1982-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1982-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1982-109">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a1982-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1982-110">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a1982-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a1982-111">Pointeur vers un appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour créer le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="a1982-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a1982-112">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1982-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1982-113">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1982-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1982-114">Pointeur vers la face de maille d’origine qui a été fractionnée pour générer la face actuelle.</span><span class="sxs-lookup"><span data-stu-id="a1982-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="a1982-115">*pVertRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1982-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1982-116">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1982-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1982-117">Pointeur vers un tableau de destination contenant les trois vertex de maillage d’origine qui sont les parents du vertex actuel.</span><span class="sxs-lookup"><span data-stu-id="a1982-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="a1982-118">*pfVertWeights* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a1982-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1982-119">Type : **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1982-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a1982-120">Pointeur vers un tableau de destination contenant des facteurs de fusion pour les vertex pVertRemap.</span><span class="sxs-lookup"><span data-stu-id="a1982-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a1982-121">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a1982-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1982-122">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1982-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a1982-123">Pointeur vers l’objet de maillage [**ID3DXMesh**](id3dxmesh.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="a1982-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1982-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1982-124">Return value</span></span>

<span data-ttu-id="a1982-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1982-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1982-126">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1982-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a1982-127">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="a1982-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="a1982-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a1982-128">Remarks</span></span>

<span data-ttu-id="a1982-129">pVertRemap et pfVertWeights peuvent être utilisés pour interpoler toute valeur par vertex sur la maille.</span><span class="sxs-lookup"><span data-stu-id="a1982-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1982-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1982-130">Requirements</span></span>



| <span data-ttu-id="a1982-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1982-131">Requirement</span></span> | <span data-ttu-id="a1982-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1982-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1982-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1982-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a1982-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1982-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a1982-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a1982-135">Library</span></span><br/> | <dl> <span data-ttu-id="a1982-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1982-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1982-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1982-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1982-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a1982-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
