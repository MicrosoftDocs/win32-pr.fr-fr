---
description: Dessinez un tableau de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite ::D méthode rawSpritesImmediate (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323425"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="d0de6-103">ID3DX10Sprite ::D méthode rawSpritesImmediate</span><span class="sxs-lookup"><span data-stu-id="d0de6-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="d0de6-104">Dessinez un tableau de sprites.</span><span class="sxs-lookup"><span data-stu-id="d0de6-104">Draw an array of sprites.</span></span> <span data-ttu-id="d0de6-105">Cela envoie immédiatement les sprites à l’appareil pour le rendu, ce qui est différent de [**ID3DX10Sprite ::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) qui ajoute uniquement un tableau de sprites à un lot de sprites à restituer lorsque [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="d0de6-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="d0de6-106">Cette méthode de dessin est particulièrement utile lors du dessin d’un grand nombre de sprites qui ont déjà été triés sur l’UC (ou qui n’ont pas besoin d’être triés), comme dans un système de particules.</span><span class="sxs-lookup"><span data-stu-id="d0de6-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="d0de6-107">Elle doit être appelée entre les appels à [**ID3DX10Sprite :: Begin**](id3dx10sprite-begin.md) et [**ID3DX10Sprite :: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="d0de6-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0de6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0de6-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="d0de6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0de6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0de6-110">*pSprites* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0de6-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0de6-111">Type : **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0de6-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="d0de6-112">Tableau de sprites à dessiner.</span><span class="sxs-lookup"><span data-stu-id="d0de6-112">The array of sprites to draw.</span></span> <span data-ttu-id="d0de6-113">Consultez [**d3dx10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="d0de6-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0de6-114">*cSprites* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0de6-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0de6-115">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0de6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0de6-116">Nombre de sprites dans pSprites.</span><span class="sxs-lookup"><span data-stu-id="d0de6-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="d0de6-117">*cbSprite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0de6-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0de6-118">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0de6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0de6-119">Taille de la structure sprite que vous passez dans pSprites.</span><span class="sxs-lookup"><span data-stu-id="d0de6-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="d0de6-120">Le passage de la valeur 0 est l’équivalent du passage de sizeof (D3DX10 \_ sprite).</span><span class="sxs-lookup"><span data-stu-id="d0de6-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="d0de6-121">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0de6-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0de6-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0de6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d0de6-123">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d0de6-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0de6-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d0de6-124">Return value</span></span>

<span data-ttu-id="d0de6-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0de6-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0de6-126">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d0de6-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d0de6-127">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="d0de6-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0de6-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0de6-128">Requirements</span></span>



| <span data-ttu-id="d0de6-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0de6-129">Requirement</span></span> | <span data-ttu-id="d0de6-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0de6-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0de6-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0de6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="d0de6-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0de6-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0de6-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d0de6-133">Library</span></span><br/> | <dl> <span data-ttu-id="d0de6-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0de6-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0de6-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0de6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0de6-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="d0de6-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="d0de6-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d0de6-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
