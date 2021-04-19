---
description: Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées ID3DXPRTCompBuffer et ajoute les données à un objet ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer :: ExtractToMesh, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542146"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a><span data-ttu-id="31ec0-103">ID3DXPRTCompBuffer :: ExtractToMesh, méthode</span><span class="sxs-lookup"><span data-stu-id="31ec0-103">ID3DXPRTCompBuffer::ExtractToMesh method</span></span>

<span data-ttu-id="31ec0-104">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="31ec0-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ec0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31ec0-105">Syntax</span></span>


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a><span data-ttu-id="31ec0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31ec0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ec0-107">*NumPCA* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31ec0-107">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ec0-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ec0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ec0-109">Nombre de coefficients d’APC à extraire de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="31ec0-109">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="31ec0-110">*Utilisation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31ec0-110">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ec0-111">Type : **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="31ec0-111">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="31ec0-112">Descriptions de l’utilisation des sommets de la maille.</span><span class="sxs-lookup"><span data-stu-id="31ec0-112">Vertex usage descriptions of the mesh.</span></span> <span data-ttu-id="31ec0-113">Consultez [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="31ec0-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="31ec0-114">*UsageIndexStart* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31ec0-114">*UsageIndexStart* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ec0-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ec0-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ec0-116">Index de départ pour les coefficients de l’APC à stocker dans la maille.</span><span class="sxs-lookup"><span data-stu-id="31ec0-116">Starting index for PCA coefficients to be stored in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="31ec0-117">*pScene* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="31ec0-117">*pScene* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ec0-118">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="31ec0-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="31ec0-119">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) qui stocke les coefficients PCA.</span><span class="sxs-lookup"><span data-stu-id="31ec0-119">Pointer to an [**ID3DXMesh**](id3dxmesh.md) mesh object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ec0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31ec0-120">Return value</span></span>

<span data-ttu-id="31ec0-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31ec0-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31ec0-122">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31ec0-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="31ec0-123">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="31ec0-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ec0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31ec0-124">Requirements</span></span>



| <span data-ttu-id="31ec0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31ec0-125">Requirement</span></span> | <span data-ttu-id="31ec0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="31ec0-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ec0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="31ec0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="31ec0-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ec0-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31ec0-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31ec0-129">Library</span></span><br/> | <dl> <span data-ttu-id="31ec0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ec0-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31ec0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31ec0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ec0-132">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="31ec0-132">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
