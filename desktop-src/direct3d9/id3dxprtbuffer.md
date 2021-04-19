---
description: L’interface ID3DXPRTBuffer est utilisée comme mémoire tampon de données pour stocker les données de vertex et de pixels à utiliser avec les méthodes et les fonctions de transfert luminance (PRT) précalculées.
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interface ID3DXPRTBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522999"
---
# <a name="id3dxprtbuffer-interface"></a><span data-ttu-id="16490-103">Interface ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="16490-103">ID3DXPRTBuffer interface</span></span>

<span data-ttu-id="16490-104">L’interface ID3DXPRTBuffer est utilisée comme mémoire tampon de données pour stocker les données de vertex et de pixels à utiliser avec les méthodes et les fonctions de transfert luminance (PRT) précalculées.</span><span class="sxs-lookup"><span data-stu-id="16490-104">The ID3DXPRTBuffer interface is used as a data buffer to store vertex and pixel data for use with precomputed radiance transfer (PRT) methods and functions.</span></span>

## <a name="members"></a><span data-ttu-id="16490-105">Membres</span><span class="sxs-lookup"><span data-stu-id="16490-105">Members</span></span>

<span data-ttu-id="16490-106">L’interface **ID3DXPRTBuffer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="16490-106">The **ID3DXPRTBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="16490-107">**ID3DXPRTBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="16490-107">**ID3DXPRTBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="16490-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16490-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="16490-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16490-109">Methods</span></span>

<span data-ttu-id="16490-110">L’interface **ID3DXPRTBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="16490-110">The **ID3DXPRTBuffer** interface has these methods.</span></span>



| <span data-ttu-id="16490-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="16490-111">Method</span></span>                                                   | <span data-ttu-id="16490-112">Description</span><span class="sxs-lookup"><span data-stu-id="16490-112">Description</span></span>                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16490-113">**AddBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-113">**AddBuffer**</span></span>](id3dxprtbuffer--addbuffer.md)           | <span data-ttu-id="16490-114">Ajoute une autre mémoire tampon au **ID3DXPRTBuffer** et stocke les résultats dans **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="16490-114">Adds another buffer to the **ID3DXPRTBuffer** and stores the results in **ID3DXPRTBuffer**.</span></span><br/>                                                                                        |
| [<span data-ttu-id="16490-115">**AttachGH**</span><span class="sxs-lookup"><span data-stu-id="16490-115">**AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)             | <span data-ttu-id="16490-116">Associe un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à l’objet **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="16490-116">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="16490-117">**EvalGH**</span><span class="sxs-lookup"><span data-stu-id="16490-117">**EvalGH**</span></span>](id3dxprtbuffer--evalgh.md)                 | <span data-ttu-id="16490-118">Applique les données de marge de texture stockées à une mémoire tampon de texture **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="16490-118">Applies stored texture gutter data to an **ID3DXPRTBuffer** texture buffer.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="16490-119">**ExtractTexture**</span><span class="sxs-lookup"><span data-stu-id="16490-119">**ExtractTexture**</span></span>](id3dxprtbuffer--extracttexture.md) | <span data-ttu-id="16490-120">Extrait des données de coefficient à partir d’un canal de couleur de la mémoire tampon pour une plage de coefficients spécifiée, et ajoute les données à un objet [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="16490-120">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span><br/> |
| [<span data-ttu-id="16490-121">**ExtractToMesh**</span><span class="sxs-lookup"><span data-stu-id="16490-121">**ExtractToMesh**</span></span>](id3dxprtbuffer--extracttomesh.md)   | <span data-ttu-id="16490-122">Extrait des données de coefficient à partir d’une mémoire tampon de canal unique et ajoute les données à un objet [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="16490-122">Extracts coefficient data from a single-channel buffer and adds the data to an [**ID3DXMesh**](id3dxmesh.md) object.</span></span><br/>                                                              |
| [<span data-ttu-id="16490-123">**GetHeight**</span><span class="sxs-lookup"><span data-stu-id="16490-123">**GetHeight**</span></span>](id3dxprtbuffer--getheight.md)           | <span data-ttu-id="16490-124">Récupère la hauteur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="16490-124">Retrieves the height of the texture, in pixels.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="16490-125">**GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="16490-125">**GetNumChannels**</span></span>](id3dxprtbuffer--getnumchannels.md) | <span data-ttu-id="16490-126">Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.</span><span class="sxs-lookup"><span data-stu-id="16490-126">Retrieves the number of color channels used in memory to store samples.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="16490-127">**GetNumCoeffs**</span><span class="sxs-lookup"><span data-stu-id="16490-127">**GetNumCoeffs**</span></span>](id3dxprtbuffer--getnumcoeffs.md)     | <span data-ttu-id="16490-128">Récupère le nombre de scalaires par canal de couleurs utilisé en mémoire pour stocker des exemples.</span><span class="sxs-lookup"><span data-stu-id="16490-128">Retrieves the number of scalars per color channel used in memory to store samples.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="16490-129">**GetNumSamples**</span><span class="sxs-lookup"><span data-stu-id="16490-129">**GetNumSamples**</span></span>](id3dxprtbuffer--getnumsamples.md)   | <span data-ttu-id="16490-130">Récupère le nombre de vertex (ou de texels) échantillonnés.</span><span class="sxs-lookup"><span data-stu-id="16490-130">Retrieves the number of vertices (or texels) sampled.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="16490-131">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="16490-131">**GetWidth**</span></span>](id3dxprtbuffer--getwidth.md)             | <span data-ttu-id="16490-132">Récupère la largeur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="16490-132">Retrieves the width of the texture, in pixels.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="16490-133">**IsTexture**</span><span class="sxs-lookup"><span data-stu-id="16490-133">**IsTexture**</span></span>](id3dxprtbuffer--istexture.md)           | <span data-ttu-id="16490-134">Indique si la mémoire tampon contient une texture.</span><span class="sxs-lookup"><span data-stu-id="16490-134">Indicates whether the buffer contains a texture.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="16490-135">**LockBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-135">**LockBuffer**</span></span>](id3dxprtbuffer--lockbuffer.md)         | <span data-ttu-id="16490-136">Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="16490-136">Locks a range of vertex or texel sample data and obtains a pointer to the location in buffer memory.</span></span><br/>                                                                               |
| [<span data-ttu-id="16490-137">**ReleaseGH**</span><span class="sxs-lookup"><span data-stu-id="16490-137">**ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)           | <span data-ttu-id="16490-138">Dissocie un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) joint avec l’objet **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="16490-138">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the **ID3DXPRTBuffer** object.</span></span><br/>                                                   |
| [<span data-ttu-id="16490-139">**Redimensionner**</span><span class="sxs-lookup"><span data-stu-id="16490-139">**Resize**</span></span>](id3dxprtbuffer--resize.md)                 | <span data-ttu-id="16490-140">Modifie le nombre d’échantillons contenus dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="16490-140">Changes the number of samples contained in the buffer.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="16490-141">**ScaleBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-141">**ScaleBuffer**</span></span>](id3dxprtbuffer--scalebuffer.md)       | <span data-ttu-id="16490-142">Multiplie chaque valeur de la mémoire tampon par une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="16490-142">Multiplies every value in the buffer by a constant value.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="16490-143">**UnlockBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-143">**UnlockBuffer**</span></span>](id3dxprtbuffer--unlockbuffer.md)     | <span data-ttu-id="16490-144">Termine la durée de vie du pointeur ppData retourné par [**ID3DXPRTBuffer :: LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="16490-144">Ends the lifespan of the ppData pointer returned by [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="16490-145">Notes</span><span class="sxs-lookup"><span data-stu-id="16490-145">Remarks</span></span>

<span data-ttu-id="16490-146">L’interface **ID3DXPRTBuffer** est obtenue en appelant les fonctions [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .</span><span class="sxs-lookup"><span data-stu-id="16490-146">The **ID3DXPRTBuffer** interface is obtained by calling the [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) functions.</span></span>

<span data-ttu-id="16490-147">Le type LPD3DXPRTBUFFER est défini comme un pointeur vers l’interface **ID3DXPRTBuffer** .</span><span class="sxs-lookup"><span data-stu-id="16490-147">The LPD3DXPRTBUFFER type is defined as a pointer to the **ID3DXPRTBuffer** interface.</span></span>


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="16490-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16490-148">Requirements</span></span>



| <span data-ttu-id="16490-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16490-149">Requirement</span></span> | <span data-ttu-id="16490-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="16490-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16490-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="16490-151">Header</span></span><br/>  | <dl> <span data-ttu-id="16490-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="16490-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="16490-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16490-153">Library</span></span><br/> | <dl> <span data-ttu-id="16490-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16490-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16490-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16490-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16490-156">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="16490-156">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="16490-157">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-157">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="16490-158">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="16490-158">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> <dt>

[<span data-ttu-id="16490-159">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="16490-159">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
