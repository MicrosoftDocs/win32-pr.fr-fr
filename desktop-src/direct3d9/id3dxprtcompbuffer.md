---
description: L’interface ID3DXPRTCompBuffer stocke une version compressée d’une mémoire tampon ID3DXPRTBuffer, à utiliser avec l’analyse des composants principaux (PCA, principal Component Analysis).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interface ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539475"
---
# <a name="id3dxprtcompbuffer-interface"></a><span data-ttu-id="b17b7-103">Interface ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="b17b7-103">ID3DXPRTCompBuffer interface</span></span>

<span data-ttu-id="b17b7-104">L’interface **ID3DXPRTCompBuffer** stocke une version compressée d’une mémoire tampon [**ID3DXPRTBuffer**](id3dxprtbuffer.md) , à utiliser avec l’analyse des composants principaux (PCA, principal Component Analysis).</span><span class="sxs-lookup"><span data-stu-id="b17b7-104">The **ID3DXPRTCompBuffer** interface stores a compressed version of a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer, for use with principal component analysis (PCA).</span></span>

## <a name="members"></a><span data-ttu-id="b17b7-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b17b7-105">Members</span></span>

<span data-ttu-id="b17b7-106">L’interface **ID3DXPRTCompBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b17b7-106">The **ID3DXPRTCompBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b17b7-107">**ID3DXPRTCompBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b17b7-107">**ID3DXPRTCompBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="b17b7-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b17b7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b17b7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b17b7-109">Methods</span></span>

<span data-ttu-id="b17b7-110">L’interface **ID3DXPRTCompBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b17b7-110">The **ID3DXPRTCompBuffer** interface has these methods.</span></span>



| <span data-ttu-id="b17b7-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="b17b7-111">Method</span></span>                                                             | <span data-ttu-id="b17b7-112">Description</span><span class="sxs-lookup"><span data-stu-id="b17b7-112">Description</span></span>                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b17b7-113">**ExtractBasis**</span><span class="sxs-lookup"><span data-stu-id="b17b7-113">**ExtractBasis**</span></span>](id3dxprtcompbuffer--extractbasis.md)           | <span data-ttu-id="b17b7-114">Extrait les vecteurs de base de la moyenne et de l’analyse des composants principaux (PCA) pour un cluster donné à partir d’une mémoire tampon de données compressées **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="b17b7-114">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                       |
| [<span data-ttu-id="b17b7-115">**ExtractClusterIDs**</span><span class="sxs-lookup"><span data-stu-id="b17b7-115">**ExtractClusterIDs**</span></span>](id3dxprtcompbuffer--extractclusterids.md) | <span data-ttu-id="b17b7-116">Extrait les ID de cluster par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="b17b7-116">Extracts the per-sample cluster IDs from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="b17b7-117">**ExtractPCA**</span><span class="sxs-lookup"><span data-stu-id="b17b7-117">**ExtractPCA**</span></span>](id3dxprtcompbuffer--extractpca.md)               | <span data-ttu-id="b17b7-118">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="b17b7-118">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer.</span></span><br/>                                                                               |
| [<span data-ttu-id="b17b7-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="b17b7-119">**ExtractTexture**</span></span>](id3dxprtcompbuffer--extracttexture.md)       | <span data-ttu-id="b17b7-120">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="b17b7-120">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="b17b7-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="b17b7-121">**ExtractToMesh**</span></span>](id3dxprtcompbuffer--extracttomesh.md)         | <span data-ttu-id="b17b7-122">Extrait les coefficients de projection de l’analyse des composants principaux (PCA) par exemple à partir d’un tampon de données compressées **ID3DXPRTCompBuffer** et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="b17b7-122">Extracts the per-sample principal component analysis (PCA) projection coefficients from an **ID3DXPRTCompBuffer** compressed data buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                 |
| [<span data-ttu-id="b17b7-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="b17b7-123">**GetHeight**</span></span>](id3dxprtcompbuffer--getheight.md)                 | <span data-ttu-id="b17b7-124">Récupère la hauteur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b17b7-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="b17b7-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="b17b7-125">**GetNumChannels**</span></span>](id3dxprtcompbuffer--getnumchannels.md)       | <span data-ttu-id="b17b7-126">Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.</span><span class="sxs-lookup"><span data-stu-id="b17b7-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="b17b7-127">**GetNumClusters**</span><span class="sxs-lookup"><span data-stu-id="b17b7-127">**GetNumClusters**</span></span>](id3dxprtcompbuffer--getnumclusters.md)       | <span data-ttu-id="b17b7-128">Récupère le nombre de clusters à utiliser pour la compression.</span><span class="sxs-lookup"><span data-stu-id="b17b7-128">Retrieves the number of clusters to use for compression.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="b17b7-129">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="b17b7-129">**GetNumCoeffs**</span></span>](id3dxprtcompbuffer--getnumcoeffs.md)           | <span data-ttu-id="b17b7-130">Récupère le nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples.</span><span class="sxs-lookup"><span data-stu-id="b17b7-130">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="b17b7-131">**GetNumPCA**</span><span class="sxs-lookup"><span data-stu-id="b17b7-131">**GetNumPCA**</span></span>](id3dxprtcompbuffer--getnumpca.md)                 | <span data-ttu-id="b17b7-132">Récupère le nombre de vecteurs de base de l’analyse des composants principaux (PCA) à utiliser dans chaque cluster.</span><span class="sxs-lookup"><span data-stu-id="b17b7-132">Retrieves the number of principal component analysis (PCA) basis vectors to use in each cluster.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="b17b7-133">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="b17b7-133">**GetNumSamples**</span></span>](id3dxprtcompbuffer--getnumsamples.md)         | <span data-ttu-id="b17b7-134">Récupère le nombre de vertex (ou de texels) échantillonnés.</span><span class="sxs-lookup"><span data-stu-id="b17b7-134">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="b17b7-135">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="b17b7-135">**GetWidth**</span></span>](id3dxprtcompbuffer--getwidth.md)                   | <span data-ttu-id="b17b7-136">Récupère la largeur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="b17b7-136">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="b17b7-137">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="b17b7-137">**IsTexture**</span></span>](id3dxprtcompbuffer--istexture.md)                 | <span data-ttu-id="b17b7-138">Indique si la mémoire tampon contient une texture.</span><span class="sxs-lookup"><span data-stu-id="b17b7-138">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="b17b7-139">**NormalizeData**</span><span class="sxs-lookup"><span data-stu-id="b17b7-139">**NormalizeData**</span></span>](id3dxprtcompbuffer--normalizedata.md)         | <span data-ttu-id="b17b7-140">Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="b17b7-140">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="b17b7-141">Les vecteurs de base sont modifiés pour refléter cette normalisation.</span><span class="sxs-lookup"><span data-stu-id="b17b7-141">Basis vectors are modified to reflect this normalization.</span></span><br/>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="b17b7-142">Notes</span><span class="sxs-lookup"><span data-stu-id="b17b7-142">Remarks</span></span>

<span data-ttu-id="b17b7-143">L’interface **ID3DXPRTCompBuffer** est obtenue en appelant la fonction [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b17b7-143">The **ID3DXPRTCompBuffer** interface is obtained by calling the [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) function.</span></span>

<span data-ttu-id="b17b7-144">Le type LPD3DXPRTCOMPBUFFER est défini comme un pointeur vers l’interface **ID3DXPRTCompBuffer** .</span><span class="sxs-lookup"><span data-stu-id="b17b7-144">The LPD3DXPRTCOMPBUFFER type is defined as a pointer to the **ID3DXPRTCompBuffer** interface.</span></span>


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="b17b7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b17b7-145">Requirements</span></span>



| <span data-ttu-id="b17b7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b17b7-146">Requirement</span></span> | <span data-ttu-id="b17b7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b17b7-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b17b7-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="b17b7-148">Header</span></span><br/>  | <dl> <span data-ttu-id="b17b7-149"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b17b7-149"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b17b7-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b17b7-150">Library</span></span><br/> | <dl> <span data-ttu-id="b17b7-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b17b7-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b17b7-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b17b7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17b7-153">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b17b7-153">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b17b7-154">**D3DXCreatePRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="b17b7-154">**D3DXCreatePRTCompBuffer**</span></span>](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="b17b7-155">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="b17b7-155">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
