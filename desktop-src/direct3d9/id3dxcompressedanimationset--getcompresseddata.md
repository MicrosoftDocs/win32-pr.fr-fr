---
description: Obtient la mémoire tampon de données qui stocke les données d’animation d’image clé compressées.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'ID3DXCompressedAnimationSet :: GetCompressedData, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522596"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="073ad-103">ID3DXCompressedAnimationSet :: GetCompressedData, méthode</span><span class="sxs-lookup"><span data-stu-id="073ad-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="073ad-104">Obtient la mémoire tampon de données qui stocke les données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="073ad-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="073ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="073ad-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="073ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="073ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="073ad-107">*ppCompressedData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="073ad-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="073ad-108">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="073ad-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="073ad-109">Adresse d’un pointeur vers la mémoire tampon de données [**ID3DXBuffer**](id3dxbuffer.md) qui reçoit des données d’animation d’image clé compressées.</span><span class="sxs-lookup"><span data-stu-id="073ad-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="073ad-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="073ad-110">Return value</span></span>

<span data-ttu-id="073ad-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="073ad-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="073ad-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="073ad-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="073ad-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="073ad-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="073ad-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="073ad-114">Requirements</span></span>



| <span data-ttu-id="073ad-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="073ad-115">Requirement</span></span> | <span data-ttu-id="073ad-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="073ad-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="073ad-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="073ad-117">Header</span></span><br/>  | <dl> <span data-ttu-id="073ad-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="073ad-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="073ad-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="073ad-119">Library</span></span><br/> | <dl> <span data-ttu-id="073ad-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="073ad-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="073ad-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="073ad-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="073ad-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="073ad-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




