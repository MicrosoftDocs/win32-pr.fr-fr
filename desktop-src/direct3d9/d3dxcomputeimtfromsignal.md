---
description: Calcule les IMTs par triangle à partir d’un signal spécifié par l’application, qui varie en fonction de la surface du maillage (généralement à une fréquence plus élevée que les données de vertex). Le signal est évalué par le biais d’une fonction de rappel spécifiée par l’utilisateur.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: D3DXComputeIMTFromSignal, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 979304a350c226a9406e62896bb84492d8046e74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538344"
---
# <a name="d3dxcomputeimtfromsignal-function"></a><span data-ttu-id="b7c72-104">D3DXComputeIMTFromSignal fonction)</span><span class="sxs-lookup"><span data-stu-id="b7c72-104">D3DXComputeIMTFromSignal function</span></span>

<span data-ttu-id="b7c72-105">Calcule les IMTs par triangle à partir d’un signal spécifié par l’application, qui varie en fonction de la surface du maillage (généralement à une fréquence plus élevée que les données de vertex).</span><span class="sxs-lookup"><span data-stu-id="b7c72-105">Calculates per-triangle IMT's from a custom application-specified signal that varies over the surface of the mesh (generally at a higher frequency than vertex data).</span></span> <span data-ttu-id="b7c72-106">Le signal est évalué par le biais d’une fonction de rappel spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b7c72-106">The signal is evaluated via a user-specified callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7c72-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7c72-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="b7c72-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7c72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7c72-109">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-110">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b7c72-111">Pointeur vers un maillage d’entrée (voir [**ID3DXMesh**](id3dxmesh.md)) qui contient la géométrie d’objet pour le calcul du IMT.</span><span class="sxs-lookup"><span data-stu-id="b7c72-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-112">*dwTextureIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c72-114">Index de coordonnées de texture de base zéro qui identifie le jeu de coordonnées de texture à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b7c72-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-115">*uSignalDimension* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-115">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c72-117">Nombre de composants dans chaque point de données dans le signal.</span><span class="sxs-lookup"><span data-stu-id="b7c72-117">The number of components in each data point in the signal.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-118">*fMaxUVDistance* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-118">*fMaxUVDistance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-119">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c72-120">Distance maximale entre les vertex ; l’algorithme continue à se subdiviser jusqu’à ce que la distance entre tous les vertex soit inférieure ou égale à fMaxUVDistance.</span><span class="sxs-lookup"><span data-stu-id="b7c72-120">The maximum distance between vertices; the algorithm continues subdividing until the distance between all vertices is less than or equal to fMaxUVDistance.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-121">*dwOptions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-121">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-122">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c72-123">Options de retour à la ligne.</span><span class="sxs-lookup"><span data-stu-id="b7c72-123">Texture wrap options.</span></span> <span data-ttu-id="b7c72-124">Il s’agit d’une combinaison d’un ou plusieurs [**indicateurs D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="b7c72-124">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-125">*pSignalCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-125">*pSignalCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-126">Type : **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-126">Type: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**</span></span>

<span data-ttu-id="b7c72-127">Pointeur vers une fonction évaluateur fournie par l’utilisateur, qui sera utilisée pour calculer la valeur de signal à des coordonnées U, V arbitraires.</span><span class="sxs-lookup"><span data-stu-id="b7c72-127">A pointer to a user-provided evaluator function, which will be used to compute the signal value at arbitrary U,V coordinates.</span></span> <span data-ttu-id="b7c72-128">La fonction suit le prototype de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span><span class="sxs-lookup"><span data-stu-id="b7c72-128">The function follows the prototype of [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-129">*pUserData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-129">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-130">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="b7c72-130">Type: **VOID\***</span></span>

<span data-ttu-id="b7c72-131">Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel de signal.</span><span class="sxs-lookup"><span data-stu-id="b7c72-131">A pointer to a user-defined value which is passed to the signal callback function.</span></span> <span data-ttu-id="b7c72-132">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="b7c72-132">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-133">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="b7c72-133">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="b7c72-134">Type : **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-134">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="b7c72-135">Pointeur vers une fonction de rappel pour surveiller la progression du calcul IMT.</span><span class="sxs-lookup"><span data-stu-id="b7c72-135">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-136">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="b7c72-136">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b7c72-137">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-137">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7c72-138">Pointeur vers une variable définie par l’utilisateur qui est passée à la fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="b7c72-138">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="b7c72-139">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="b7c72-139">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b7c72-140">*ppIMTData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7c72-140">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7c72-141">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7c72-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b7c72-142">Pointeur vers la mémoire tampon (consultez [**ID3DXBuffer**](id3dxbuffer.md)) contenant le tableau IMT retourné.</span><span class="sxs-lookup"><span data-stu-id="b7c72-142">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="b7c72-143">Ce tableau peut être fourni comme entrée aux fonctions D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) pour classer par ordre de priorité l’allocation d’espace de texture dans le paramétrage de la texture.</span><span class="sxs-lookup"><span data-stu-id="b7c72-143">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7c72-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7c72-144">Return value</span></span>

<span data-ttu-id="b7c72-145">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7c72-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7c72-146">Si la fonction est réussie, la valeur de retour est D3D \_ OK ; sinon, la valeur est D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b7c72-146">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7c72-147">Notes</span><span class="sxs-lookup"><span data-stu-id="b7c72-147">Remarks</span></span>

<span data-ttu-id="b7c72-148">Cette fonction requiert que le maillage d’entrée contienne un mappage de texture signal-à-maillage (coordonnées de texture).</span><span class="sxs-lookup"><span data-stu-id="b7c72-148">This function requires that the input mesh contain a signal-to-mesh texture mapping (ie. texture coordinates).</span></span> <span data-ttu-id="b7c72-149">Elle permet à l’utilisateur de définir un signal arbitrairement sur la surface de la maille.</span><span class="sxs-lookup"><span data-stu-id="b7c72-149">It allows the user to define a signal arbitrarily over the surface of the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7c72-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7c72-150">Requirements</span></span>



| <span data-ttu-id="b7c72-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7c72-151">Requirement</span></span> | <span data-ttu-id="b7c72-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7c72-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7c72-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7c72-153">Header</span></span><br/>  | <dl> <span data-ttu-id="b7c72-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7c72-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b7c72-155">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7c72-155">Library</span></span><br/> | <dl> <span data-ttu-id="b7c72-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7c72-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7c72-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7c72-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7c72-158">UVAtlas, fonctions</span><span class="sxs-lookup"><span data-stu-id="b7c72-158">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="b7c72-159">Utilisation de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b7c72-159">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
