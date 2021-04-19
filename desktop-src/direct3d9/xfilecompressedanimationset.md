---
description: Identifie les données d’animation d’image clé compressées.
ms.assetid: 2aab46db-e0ad-4bbb-b1c5-a254ec6cb984
title: XFILECOMPRESSEDANIMATIONSET, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XFILECOMPRESSEDANIMATIONSET
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 240cac57c9c0d123203ee4599c14092df1327f94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539161"
---
# <a name="xfilecompressedanimationset-structure"></a><span data-ttu-id="9ffce-103">XFILECOMPRESSEDANIMATIONSET, structure</span><span class="sxs-lookup"><span data-stu-id="9ffce-103">XFILECOMPRESSEDANIMATIONSET structure</span></span>

<span data-ttu-id="9ffce-104">Identifie les données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="9ffce-104">Identifies compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ffce-105">Syntax</span></span>


```C++
typedef struct XFILECOMPRESSEDANIMATIONSET {
  DWORD CompressedBlockSize;
  FLOAT TicksPerSec;
  DWORD PlaybackType;
  DWORD BufferLength;
} XFILECOMPRESSEDANIMATIONSET, *LPXFILECOMPRESSEDANIMATIONSET;
```



## <a name="members"></a><span data-ttu-id="9ffce-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9ffce-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ffce-107">**CompressedBlockSize**</span><span class="sxs-lookup"><span data-stu-id="9ffce-107">**CompressedBlockSize**</span></span>
</dt> <dd>

<span data-ttu-id="9ffce-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ffce-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ffce-109">Taille totale, en octets, des données compressées dans le tampon de données d’animation d’image clé compressée.</span><span class="sxs-lookup"><span data-stu-id="9ffce-109">Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9ffce-110">**TicksPerSec**</span><span class="sxs-lookup"><span data-stu-id="9ffce-110">**TicksPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="9ffce-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ffce-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ffce-112">Nombre de battements d’image clé d’animation qui se produisent par seconde.</span><span class="sxs-lookup"><span data-stu-id="9ffce-112">Number of animation key frame ticks that occur per second.</span></span>

</dd> <dt>

<span data-ttu-id="9ffce-113">**PlaybackType**</span><span class="sxs-lookup"><span data-stu-id="9ffce-113">**PlaybackType**</span></span>
</dt> <dd>

<span data-ttu-id="9ffce-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ffce-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ffce-115">Type de la boucle de lecture du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="9ffce-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="9ffce-116">Consultez [**\_ type D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="9ffce-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ffce-117">**BufferLength**</span><span class="sxs-lookup"><span data-stu-id="9ffce-117">**BufferLength**</span></span>
</dt> <dd>

<span data-ttu-id="9ffce-118">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ffce-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ffce-119">Taille minimale de la mémoire tampon, en octets, nécessaire pour contenir les données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="9ffce-119">Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="9ffce-120">La valeur est égale à ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="9ffce-120">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ffce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ffce-121">Requirements</span></span>



| <span data-ttu-id="9ffce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ffce-122">Requirement</span></span> | <span data-ttu-id="9ffce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ffce-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffce-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ffce-124">Header</span></span><br/> | <dl> <span data-ttu-id="9ffce-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ffce-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ffce-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ffce-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ffce-127">Structures de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="9ffce-127">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="9ffce-128">**ID3DXCompressedAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="9ffce-128">**ID3DXCompressedAnimationSet**</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 
