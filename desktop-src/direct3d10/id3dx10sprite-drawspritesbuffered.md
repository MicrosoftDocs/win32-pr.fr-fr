---
description: Ajoutez un tableau de sprites au lot de sprites à restituer.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite ::D méthode rawSpritesBuffered (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535845"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="e5c92-103">ID3DX10Sprite ::D méthode rawSpritesBuffered</span><span class="sxs-lookup"><span data-stu-id="e5c92-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="e5c92-104">Ajoutez un tableau de sprites au lot de sprites à restituer.</span><span class="sxs-lookup"><span data-stu-id="e5c92-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="e5c92-105">Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md), et [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) doit être appelé avant end pour envoyer tous les sprites traités par lot à l’appareil pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="e5c92-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="e5c92-106">Cette méthode de dessin est particulièrement utile lorsque vous dessinez un petit nombre de sprites que vous souhaitez mettre en mémoire tampon dans un grand lot, tel que des polices.</span><span class="sxs-lookup"><span data-stu-id="e5c92-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5c92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5c92-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="e5c92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5c92-109">*pSprites* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5c92-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c92-110">Type : **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5c92-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="e5c92-111">Tableau de sprites à dessiner.</span><span class="sxs-lookup"><span data-stu-id="e5c92-111">The array of sprites to draw.</span></span> <span data-ttu-id="e5c92-112">Consultez [**d3dx10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="e5c92-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5c92-113">*cSprites* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5c92-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5c92-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5c92-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5c92-115">Nombre de sprites dans pSprites.</span><span class="sxs-lookup"><span data-stu-id="e5c92-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5c92-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5c92-116">Return value</span></span>

<span data-ttu-id="e5c92-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5c92-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5c92-118">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5c92-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e5c92-119">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="e5c92-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5c92-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5c92-120">Requirements</span></span>



| <span data-ttu-id="e5c92-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5c92-121">Requirement</span></span> | <span data-ttu-id="e5c92-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5c92-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5c92-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5c92-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e5c92-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5c92-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5c92-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e5c92-125">Library</span></span><br/> | <dl> <span data-ttu-id="e5c92-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5c92-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5c92-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5c92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c92-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="e5c92-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="e5c92-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="e5c92-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
