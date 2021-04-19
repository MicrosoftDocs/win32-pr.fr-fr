---
description: Obtient la transformation de vue qui s’applique à tous les sprites.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'ID3DX10Sprite :: GetViewTransform, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543573"
---
# <a name="id3dx10spritegetviewtransform-method"></a><span data-ttu-id="bc320-103">ID3DX10Sprite :: GetViewTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="bc320-103">ID3DX10Sprite::GetViewTransform method</span></span>

<span data-ttu-id="bc320-104">Obtient la transformation de vue qui s’applique à tous les sprites.</span><span class="sxs-lookup"><span data-stu-id="bc320-104">Get the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc320-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc320-105">Syntax</span></span>


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="bc320-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc320-107">*pViewTransform* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc320-107">*pViewTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc320-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc320-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bc320-109">Pointeur vers un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) qui sera défini sur la transformation du sprite à partir de l’espace universel d’origine.</span><span class="sxs-lookup"><span data-stu-id="bc320-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc320-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc320-110">Return value</span></span>

<span data-ttu-id="bc320-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc320-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc320-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bc320-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bc320-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="bc320-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc320-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc320-114">Requirements</span></span>



| <span data-ttu-id="bc320-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc320-115">Requirement</span></span> | <span data-ttu-id="bc320-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc320-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc320-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc320-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bc320-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc320-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc320-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bc320-119">Library</span></span><br/> | <dl> <span data-ttu-id="bc320-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc320-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc320-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc320-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc320-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="bc320-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="bc320-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="bc320-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
