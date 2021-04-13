---
description: Crée une mémoire tampon luminance de transfert précalculée (PRT) compressée à partir d’un objet ID3DXPRTBuffer non compressé. Cette fonction doit être utilisée avec des tampons par vertex ou de volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: D3DXCreatePRTCompBuffer, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322945"
---
# <a name="d3dxcreateprtcompbuffer-function"></a><span data-ttu-id="47e29-104">D3DXCreatePRTCompBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="47e29-104">D3DXCreatePRTCompBuffer function</span></span>

<span data-ttu-id="47e29-105">Crée une mémoire tampon luminance de transfert précalculée (PRT) compressée à partir d’un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compressé.</span><span class="sxs-lookup"><span data-stu-id="47e29-105">Creates a compressed precomputed radiance transfer (PRT) buffer from an uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="47e29-106">Cette fonction doit être utilisée avec des tampons par vertex ou de volume.</span><span class="sxs-lookup"><span data-stu-id="47e29-106">This function should be used with per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47e29-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="47e29-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47e29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e29-109">*Qualité* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-109">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-110">Type : **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-110">Type: **[**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**</span></span>

<span data-ttu-id="47e29-111">Qualité de la compression de l’harmonique sphérique (SH).</span><span class="sxs-lookup"><span data-stu-id="47e29-111">Quality of spherical harmonic (SH) compression.</span></span> <span data-ttu-id="47e29-112">Consultez [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span><span class="sxs-lookup"><span data-stu-id="47e29-112">See [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).</span></span>

</dd> <dt>

<span data-ttu-id="47e29-113">*NumClusters* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-113">*NumClusters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e29-115">Nombre de clusters à utiliser pour la compression.</span><span class="sxs-lookup"><span data-stu-id="47e29-115">Number of clusters to use for compression.</span></span>

</dd> <dt>

<span data-ttu-id="47e29-116">*NumPCA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-116">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e29-118">Nombre de vecteurs de base de l’analyse des composants principaux (PCA) à utiliser dans chaque cluster.</span><span class="sxs-lookup"><span data-stu-id="47e29-118">Number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span>

</dd> <dt>

<span data-ttu-id="47e29-119">*PCB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-119">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-120">Type : **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-120">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="47e29-121">Pointeur facultatif vers la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) utilisée pour calculer le pourcentage de calculs de compression PRT terminés.</span><span class="sxs-lookup"><span data-stu-id="47e29-121">Optional pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that is used to compute the percentage of PRT compression computations completed.</span></span> <span data-ttu-id="47e29-122">La fonction de rappel doit être implémentée pour retourner \_ la valeur OK afin de continuer l’exécution de la routine de compression.</span><span class="sxs-lookup"><span data-stu-id="47e29-122">The callback function must be implemented to return S\_OK to keep running the compression routine.</span></span> <span data-ttu-id="47e29-123">Toute autre valeur arrêtera la compression.</span><span class="sxs-lookup"><span data-stu-id="47e29-123">Any other value will halt compression.</span></span> <span data-ttu-id="47e29-124">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="47e29-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47e29-125">*lpUserContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-125">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-126">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e29-127">Pointeur facultatif vers une valeur définie par l’utilisateur passée à la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) .</span><span class="sxs-lookup"><span data-stu-id="47e29-127">Optional pointer to a user-defined value passed to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function.</span></span> <span data-ttu-id="47e29-128">Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="47e29-128">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span> <span data-ttu-id="47e29-129">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="47e29-129">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47e29-130">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47e29-130">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-131">Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="47e29-131">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="47e29-132">Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) non compressé qui sera compressé.</span><span class="sxs-lookup"><span data-stu-id="47e29-132">Address of a pointer to the uncompressed [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that will be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="47e29-133">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="47e29-133">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="47e29-134">Type : **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47e29-134">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="47e29-135">Adresse d’un pointeur vers l’objet [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de sortie.</span><span class="sxs-lookup"><span data-stu-id="47e29-135">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e29-136">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47e29-136">Return value</span></span>

<span data-ttu-id="47e29-137">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47e29-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47e29-138">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47e29-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47e29-139">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="47e29-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e29-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47e29-140">Requirements</span></span>



| <span data-ttu-id="47e29-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47e29-141">Requirement</span></span> | <span data-ttu-id="47e29-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="47e29-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47e29-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="47e29-143">Header</span></span><br/>  | <dl> <span data-ttu-id="47e29-144"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e29-144"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="47e29-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47e29-145">Library</span></span><br/> | <dl> <span data-ttu-id="47e29-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47e29-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47e29-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47e29-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e29-148">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="47e29-148">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="47e29-149">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="47e29-149">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="47e29-150">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="47e29-150">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
