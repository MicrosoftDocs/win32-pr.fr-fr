---
description: Définit la transformation Sprite.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: 'ID3DXSprite :: SetTransform, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 316e7e2c68dfa8f25a712c2077ece03d09455050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211825"
---
# <a name="id3dxspritesettransform-method"></a><span data-ttu-id="0a6f6-103">ID3DXSprite :: SetTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="0a6f6-103">ID3DXSprite::SetTransform method</span></span>

<span data-ttu-id="0a6f6-104">Définit la transformation Sprite.</span><span class="sxs-lookup"><span data-stu-id="0a6f6-104">Sets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a6f6-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="0a6f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a6f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6f6-107">*pTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a6f6-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6f6-108">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a6f6-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0a6f6-109">Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation du sprite à partir de l’espace universel d’origine.</span><span class="sxs-lookup"><span data-stu-id="0a6f6-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="0a6f6-110">Utilisez cette transformation pour mettre à l’échelle, faire pivoter ou transformer le sprite.</span><span class="sxs-lookup"><span data-stu-id="0a6f6-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6f6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a6f6-111">Return value</span></span>

<span data-ttu-id="0a6f6-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a6f6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a6f6-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a6f6-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0a6f6-114">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="0a6f6-114">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6f6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a6f6-115">Requirements</span></span>



| <span data-ttu-id="0a6f6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a6f6-116">Requirement</span></span> | <span data-ttu-id="0a6f6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a6f6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6f6-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a6f6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0a6f6-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a6f6-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0a6f6-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a6f6-120">Library</span></span><br/> | <dl> <span data-ttu-id="0a6f6-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a6f6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a6f6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a6f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6f6-123">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="0a6f6-123">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="0a6f6-124">Transformations (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0a6f6-124">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 




