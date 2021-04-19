---
description: Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé stocké dans un format de données compressé.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interface ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106533711"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="2f132-103">Interface ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="2f132-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="2f132-104">Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé stocké dans un format de données compressé.</span><span class="sxs-lookup"><span data-stu-id="2f132-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="2f132-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2f132-105">Members</span></span>

<span data-ttu-id="2f132-106">L’interface **ID3DXCompressedAnimationSet** hérite de [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="2f132-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="2f132-107">**ID3DXCompressedAnimationSet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f132-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="2f132-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f132-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f132-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f132-109">Methods</span></span>

<span data-ttu-id="2f132-110">L’interface **ID3DXCompressedAnimationSet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f132-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="2f132-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f132-111">Method</span></span>                                                                                  | <span data-ttu-id="2f132-112">Description</span><span class="sxs-lookup"><span data-stu-id="2f132-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2f132-113">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="2f132-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="2f132-114">Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.</span><span class="sxs-lookup"><span data-stu-id="2f132-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="2f132-115">**GetCompressedData**</span><span class="sxs-lookup"><span data-stu-id="2f132-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="2f132-116">Obtient la mémoire tampon de données qui stocke les données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="2f132-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="2f132-117">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="2f132-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="2f132-118">Obtient le nombre de clés de rappel dans l’ensemble d’animations.</span><span class="sxs-lookup"><span data-stu-id="2f132-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="2f132-119">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="2f132-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="2f132-120">Obtient le type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="2f132-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="2f132-121">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="2f132-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="2f132-122">Obtient le nombre de graduations d’image clé d’animation qui se produisent par seconde.</span><span class="sxs-lookup"><span data-stu-id="2f132-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="2f132-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2f132-123">Remarks</span></span>

<span data-ttu-id="2f132-124">Créer une animation d’image clé au format compressé définie avec [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="2f132-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="2f132-125">Le type LPD3DXCOMPRESSEDANIMATIONSET est défini en tant que pointeur vers cette interface.</span><span class="sxs-lookup"><span data-stu-id="2f132-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="2f132-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f132-126">Requirements</span></span>



| <span data-ttu-id="2f132-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f132-127">Requirement</span></span> | <span data-ttu-id="2f132-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f132-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f132-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f132-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2f132-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f132-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2f132-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f132-131">Library</span></span><br/> | <dl> <span data-ttu-id="2f132-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f132-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f132-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f132-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f132-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="2f132-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="2f132-135">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2f132-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




