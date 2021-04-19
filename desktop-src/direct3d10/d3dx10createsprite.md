---
description: Créer un sprite pour dessiner une texture 2D. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser Direct2D et la bibliothèque DirectXTK, la classe SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: D3DX10CreateSprite, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535800"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="a679c-103">D3DX10CreateSprite fonction)</span><span class="sxs-lookup"><span data-stu-id="a679c-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="a679c-104">Créer un sprite pour dessiner une texture 2D.</span><span class="sxs-lookup"><span data-stu-id="a679c-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="a679c-105">Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [Direct2D](../direct2d/direct2d-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteBatch** .</span><span class="sxs-lookup"><span data-stu-id="a679c-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a679c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a679c-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="a679c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a679c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a679c-108">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a679c-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a679c-109">Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a679c-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a679c-110">Pointeur vers l’appareil (voir [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) qui dessinera le sprite.</span><span class="sxs-lookup"><span data-stu-id="a679c-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="a679c-111">*cDeviceBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a679c-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a679c-112">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a679c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a679c-113">Taille de la mémoire tampon de vertex, en nombre de sprites, qui sera envoyée à l’appareil lorsque [**ID3DX10Sprite :: Flush**](id3dx10sprite-flush.md) ou [**ID3DX10Sprite ::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="a679c-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="a679c-114">Ce nombre doit être faible si vous savez que vous allez afficher un petit nombre de sprites à la fois (pour économiser la mémoire) et un grand nombre si vous savez que vous allez afficher un grand nombre de sprites à la fois.</span><span class="sxs-lookup"><span data-stu-id="a679c-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="a679c-115">La valeur maximale est 4096.</span><span class="sxs-lookup"><span data-stu-id="a679c-115">The maximum value is 4096.</span></span> <span data-ttu-id="a679c-116">Si la valeur 0 est spécifiée, la taille de la mémoire tampon du vertex sera automatiquement définie sur 4096.</span><span class="sxs-lookup"><span data-stu-id="a679c-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="a679c-117">*ppSprite* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a679c-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a679c-118">Type : **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="a679c-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="a679c-119">Adresse d’un pointeur vers une interface Sprite (voir [**interface ID3DX10Sprite**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="a679c-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a679c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a679c-120">Return value</span></span>

<span data-ttu-id="a679c-121">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a679c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a679c-122">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a679c-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a679c-123">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a679c-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a679c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a679c-124">Requirements</span></span>



| <span data-ttu-id="a679c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a679c-125">Requirement</span></span> | <span data-ttu-id="a679c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a679c-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a679c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a679c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a679c-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a679c-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a679c-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a679c-129">Library</span></span><br/> | <dl> <span data-ttu-id="a679c-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a679c-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a679c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a679c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a679c-132">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="a679c-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
