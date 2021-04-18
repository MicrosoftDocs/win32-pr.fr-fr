---
description: Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur. Cette fonction doit être utilisée pour créer des mémoires tampons par pixel.
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: D3DXCreatePRTBufferTex, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522593"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="42d5e-104">D3DXCreatePRTBufferTex fonction)</span><span class="sxs-lookup"><span data-stu-id="42d5e-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="42d5e-105">Crée une mémoire tampon de transfert luminance (PRT) précalculée qui peut être compressée ou remplie par un simulateur.</span><span class="sxs-lookup"><span data-stu-id="42d5e-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="42d5e-106">Cette fonction doit être utilisée pour créer des mémoires tampons par pixel.</span><span class="sxs-lookup"><span data-stu-id="42d5e-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d5e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42d5e-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="42d5e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42d5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d5e-109">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42d5e-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d5e-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42d5e-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42d5e-111">Largeur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="42d5e-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="42d5e-112">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42d5e-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d5e-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42d5e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42d5e-114">Hauteur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="42d5e-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="42d5e-115">*NumCoeffs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42d5e-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d5e-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42d5e-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42d5e-117">Nombre de coefficients par emplacement d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="42d5e-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="42d5e-118">Lors de l’utilisation de l’harmonique sphérique (SH) PRT, le nombre de coefficients doit être Order ², où Order est l’ordre de l’évaluation SH.</span><span class="sxs-lookup"><span data-stu-id="42d5e-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="42d5e-119">La commande doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="42d5e-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="42d5e-120">Le degré de l’évaluation est Order-1.</span><span class="sxs-lookup"><span data-stu-id="42d5e-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="42d5e-121">*NumChannels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42d5e-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42d5e-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42d5e-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42d5e-123">Nombre de canaux de couleur à définir dans le maillage.</span><span class="sxs-lookup"><span data-stu-id="42d5e-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="42d5e-124">Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="42d5e-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="42d5e-125">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="42d5e-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42d5e-126">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="42d5e-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="42d5e-127">Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) créé.</span><span class="sxs-lookup"><span data-stu-id="42d5e-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d5e-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42d5e-128">Return value</span></span>

<span data-ttu-id="42d5e-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42d5e-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42d5e-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42d5e-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="42d5e-131">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="42d5e-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d5e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="42d5e-132">Remarks</span></span>

<span data-ttu-id="42d5e-133">Lorsque la mémoire tampon est créée, toutes les valeurs sont initialisées à zéro.</span><span class="sxs-lookup"><span data-stu-id="42d5e-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d5e-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42d5e-134">Requirements</span></span>



| <span data-ttu-id="42d5e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42d5e-135">Requirement</span></span> | <span data-ttu-id="42d5e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="42d5e-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42d5e-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="42d5e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="42d5e-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d5e-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="42d5e-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="42d5e-139">Library</span></span><br/> | <dl> <span data-ttu-id="42d5e-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42d5e-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="42d5e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42d5e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d5e-142">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="42d5e-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="42d5e-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="42d5e-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
