---
description: 'Fonction D3DXSHPRTCompSplitMeshSC : utilisée avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.'
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: D3DXSHPRTCompSplitMeshSC, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093897"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="6c1af-103">D3DXSHPRTCompSplitMeshSC fonction)</span><span class="sxs-lookup"><span data-stu-id="6c1af-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="6c1af-104">Utilisé avec les résultats compressés de la version vertex du simulateur de transfert luminance (PRT) précalculé.</span><span class="sxs-lookup"><span data-stu-id="6c1af-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="6c1af-105">Une fois [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) appelé, cette fonction peut être utilisée pour fractionner le maillage en un groupe de faces/vertex par Super cluster.</span><span class="sxs-lookup"><span data-stu-id="6c1af-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="6c1af-106">Chaque supercluster contient tous les visages qui contiennent des vertex classés dans l’un de ses clusters.</span><span class="sxs-lookup"><span data-stu-id="6c1af-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="6c1af-107">Tous les vertex connectés à cet ensemble de visages sont également inclus dans le tableau retourné ppVertStatus indiquant si le vertex appartient au Super cluster.</span><span class="sxs-lookup"><span data-stu-id="6c1af-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1af-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c1af-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="6c1af-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c1af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c1af-110">*pClusterIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-111">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c1af-112">ID de cluster *NumVertices* (extraits d’une mémoire tampon compressée.)</span><span class="sxs-lookup"><span data-stu-id="6c1af-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-113">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-115">Nombre de vertex dans le maillage d’origine.</span><span class="sxs-lookup"><span data-stu-id="6c1af-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-116">*NumCs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-118">Nombre de clusters (paramètre d’entrée à compresser).</span><span class="sxs-lookup"><span data-stu-id="6c1af-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-119">*pSClusterIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-120">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c1af-121">Tableau de taille *NumCs* qui contiendra les ID de Super cluster.</span><span class="sxs-lookup"><span data-stu-id="6c1af-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-122">*NumSCs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-124">Nombre de Super clusters alloués dans [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="6c1af-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-125">*pInputIB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-126">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-127">Tampon d’index brut pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="6c1af-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="6c1af-128">Le format dépend de *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="6c1af-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-129">*InputIBIs32Bit* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-130">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-131">Si la **valeur est true**, la mémoire tampon d’index est définie sur 32 bits ; dans le cas contraire, 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6c1af-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-132">*NumFaces* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-133">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-134">Nombre de faces dans le maillage d’origine (*pInputIB* est 3 fois cette longueur.)</span><span class="sxs-lookup"><span data-stu-id="6c1af-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-135">*ppIBData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-136">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c1af-137">Mémoire tampon d’index brute qui contiendra les visages de fractionnement résultants.</span><span class="sxs-lookup"><span data-stu-id="6c1af-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="6c1af-138">Format déterminé par *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="6c1af-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="6c1af-139">Alloué par la fonction.</span><span class="sxs-lookup"><span data-stu-id="6c1af-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-140">*pIBDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-141">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c1af-142">Longueur de *ppIBData*, assignée dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="6c1af-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-143">*OutputIBIs32Bit* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-144">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c1af-145">Si la **valeur est true**, alloue un tableau d’entiers non signés ; Sinon, alloue un tableau de type short non signé.</span><span class="sxs-lookup"><span data-stu-id="6c1af-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-146">*ppFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-147">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c1af-148">Mappage de chaque visage dans *ppIBData* aux visages d’origine.</span><span class="sxs-lookup"><span data-stu-id="6c1af-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="6c1af-149">La longueur est \* *pIBDataLength*/3.</span><span class="sxs-lookup"><span data-stu-id="6c1af-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-150">*ppVertData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-151">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c1af-152">Nouvelle structure de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="6c1af-152">New vertex data structure.</span></span> <span data-ttu-id="6c1af-153">Taille de *pVertDataLength*.</span><span class="sxs-lookup"><span data-stu-id="6c1af-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-154">*pVertDataLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-155">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c1af-156">Nombre de nouveaux vertex dans le maillage fractionné.</span><span class="sxs-lookup"><span data-stu-id="6c1af-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="6c1af-157">Assigné dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="6c1af-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-158">*pSCClusterList* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-159">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c1af-160">Tableau de longueur *NumCs* dans lequel *pSCData* indexe ( \* champs pClusterIDs) pour chaque supercluster, contient des clusters triés par supercluster.</span><span class="sxs-lookup"><span data-stu-id="6c1af-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="6c1af-161">*pSCData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c1af-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c1af-162">Type : **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c1af-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="6c1af-163">Structure par Super cluster.</span><span class="sxs-lookup"><span data-stu-id="6c1af-163">Structure per super cluster.</span></span> <span data-ttu-id="6c1af-164">Contient des index dans *ppIBData*, *pSCClusterList* et *ppVertData*.</span><span class="sxs-lookup"><span data-stu-id="6c1af-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c1af-165">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c1af-165">Return value</span></span>

<span data-ttu-id="6c1af-166">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c1af-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c1af-167">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6c1af-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c1af-168">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6c1af-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c1af-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c1af-169">Requirements</span></span>



| <span data-ttu-id="6c1af-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c1af-170">Requirement</span></span> | <span data-ttu-id="6c1af-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c1af-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c1af-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c1af-172">Header</span></span><br/>  | <dl> <span data-ttu-id="6c1af-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c1af-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c1af-174">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c1af-174">Library</span></span><br/> | <dl> <span data-ttu-id="6c1af-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c1af-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c1af-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c1af-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c1af-177">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="6c1af-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
