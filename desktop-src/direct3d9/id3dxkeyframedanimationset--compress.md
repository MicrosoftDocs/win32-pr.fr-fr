---
description: Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'ID3DXKeyframedAnimationSet :: compress, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527952"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="0ed51-103">ID3DXKeyframedAnimationSet :: compress, méthode</span><span class="sxs-lookup"><span data-stu-id="0ed51-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="0ed51-104">Transforme les animations dans une animation définie dans un format compressé et retourne un pointeur vers la mémoire tampon qui stocke les données compressées.</span><span class="sxs-lookup"><span data-stu-id="0ed51-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ed51-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="0ed51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ed51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed51-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0ed51-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed51-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ed51-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ed51-109">L’une des valeurs d' [**\_ indicateurs D3DXCOMPRESSION**](./d3dxcompression-flags.md) qui définissent le mode de compression utilisé pour le stockage des données d’animation compressées.</span><span class="sxs-lookup"><span data-stu-id="0ed51-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="0ed51-110">D3DXCOMPRESS \_ par défaut est la seule valeur actuellement prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0ed51-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="0ed51-111">*Lossiness* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ed51-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed51-112">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ed51-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ed51-113">Taux de perte de compression souhaité, dans la plage comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="0ed51-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="0ed51-114">*pHierarchy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ed51-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed51-115">Type : **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="0ed51-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="0ed51-116">Pointeur désignant une hiérarchie d’images de transformation [**D3DXFRAME**](d3dxframe.md) .</span><span class="sxs-lookup"><span data-stu-id="0ed51-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="0ed51-117">Peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0ed51-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ed51-118">*ppCompressedData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ed51-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed51-119">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ed51-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0ed51-120">Adresse d’un pointeur vers l’ensemble d’animations compressées [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0ed51-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ed51-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ed51-121">Return value</span></span>

<span data-ttu-id="0ed51-122">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ed51-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ed51-123">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ed51-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0ed51-124">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ed51-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed51-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ed51-125">Requirements</span></span>



| <span data-ttu-id="0ed51-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ed51-126">Requirement</span></span> | <span data-ttu-id="0ed51-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ed51-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed51-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ed51-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0ed51-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed51-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0ed51-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ed51-130">Library</span></span><br/> | <dl> <span data-ttu-id="0ed51-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ed51-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ed51-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ed51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed51-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0ed51-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
