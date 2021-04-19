---
description: Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur. Cette fonction doit être utilisée pour créer des mémoires tampons par vertex ou de volume.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: D3DXCreatePRTBuffer, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545284"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="bc986-104">D3DXCreatePRTBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="bc986-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="bc986-105">Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur.</span><span class="sxs-lookup"><span data-stu-id="bc986-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="bc986-106">Cette fonction doit être utilisée pour créer des mémoires tampons par vertex ou de volume.</span><span class="sxs-lookup"><span data-stu-id="bc986-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc986-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc986-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="bc986-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc986-109">*Échantillons* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc986-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc986-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc986-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc986-111">Nombre de vertex (ou de texels) échantillonnés.</span><span class="sxs-lookup"><span data-stu-id="bc986-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="bc986-112">*NumCoeffs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc986-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc986-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc986-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc986-114">Nombre de coefficients par emplacement d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="bc986-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="bc986-115">Lors de l’utilisation de l’harmonique sphérique (SH) PRT, le nombre de coefficients doit être Order ², où Order est l’ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="bc986-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="bc986-116">La commande doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="bc986-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="bc986-117">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="bc986-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="bc986-118">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bc986-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc986-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc986-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc986-120">Nombre de canaux de couleur à définir dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="bc986-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="bc986-121">Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="bc986-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="bc986-122">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc986-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc986-123">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc986-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="bc986-124">Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) créé.</span><span class="sxs-lookup"><span data-stu-id="bc986-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc986-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc986-125">Return value</span></span>

<span data-ttu-id="bc986-126">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc986-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc986-127">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc986-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc986-128">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bc986-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc986-129">Notes</span><span class="sxs-lookup"><span data-stu-id="bc986-129">Remarks</span></span>

<span data-ttu-id="bc986-130">Lorsque la mémoire tampon est créée, toutes les valeurs sont initialisées à zéro.</span><span class="sxs-lookup"><span data-stu-id="bc986-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc986-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc986-131">Requirements</span></span>



| <span data-ttu-id="bc986-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc986-132">Requirement</span></span> | <span data-ttu-id="bc986-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc986-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc986-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc986-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bc986-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc986-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bc986-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc986-136">Library</span></span><br/> | <dl> <span data-ttu-id="bc986-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc986-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc986-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc986-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc986-139">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="bc986-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="bc986-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="bc986-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
