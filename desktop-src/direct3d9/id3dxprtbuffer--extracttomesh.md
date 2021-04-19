---
description: Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer :: ExtractToMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531375"
---
# <a name="id3dxprtbufferextracttomesh-method"></a><span data-ttu-id="2ea28-103">ID3DXPRTBuffer :: ExtractToMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="2ea28-103">ID3DXPRTBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="2ea28-104">Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="2ea28-104">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ea28-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="2ea28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ea28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea28-107">*NumCoefficients* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ea28-107">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea28-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ea28-109">Nombre de coefficients à extraire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2ea28-109">Number of coefficients to extract from the buffer.</span></span> <span data-ttu-id="2ea28-110">Lorsque vous utilisez le transfert luminance précalculé (SH), le nombre de coefficients doit être Order ².</span><span class="sxs-lookup"><span data-stu-id="2ea28-110">When using spherical harmonic (SH) precomputed radiance transfer (PRT), the number of coefficients should be Order ².</span></span> <span data-ttu-id="2ea28-111">La commande doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus.</span><span class="sxs-lookup"><span data-stu-id="2ea28-111">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="2ea28-112">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ea28-112">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea28-113">Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-113">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="2ea28-114">Descriptions de l’utilisation des sommets de la maille.</span><span class="sxs-lookup"><span data-stu-id="2ea28-114">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="2ea28-115">Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="2ea28-115">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ea28-116">*UsageIndexStart* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ea28-116">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea28-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ea28-118">Index de départ pour les coefficients à stocker dans la maille.</span><span class="sxs-lookup"><span data-stu-id="2ea28-118">Starting index for coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2ea28-119">*pScene* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ea28-119">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea28-120">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="2ea28-121">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) qui stocke les coefficients.</span><span class="sxs-lookup"><span data-stu-id="2ea28-121">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea28-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ea28-122">Return value</span></span>

<span data-ttu-id="2ea28-123">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ea28-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ea28-124">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ea28-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2ea28-125">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2ea28-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea28-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ea28-126">Requirements</span></span>



| <span data-ttu-id="2ea28-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ea28-127">Requirement</span></span> | <span data-ttu-id="2ea28-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ea28-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea28-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ea28-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2ea28-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea28-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2ea28-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2ea28-131">Library</span></span><br/> | <dl> <span data-ttu-id="2ea28-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ea28-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ea28-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ea28-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea28-134">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="2ea28-134">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
