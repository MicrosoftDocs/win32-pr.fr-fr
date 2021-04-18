---
description: Définissez la transformation de vue qui s’applique à tous les sprites.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'ID3DX10Sprite :: SetViewTransform, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106533720"
---
# <a name="id3dx10spritesetviewtransform-method"></a><span data-ttu-id="5462f-103">ID3DX10Sprite :: SetViewTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="5462f-103">ID3DX10Sprite::SetViewTransform method</span></span>

<span data-ttu-id="5462f-104">Définissez la transformation de vue qui s’applique à tous les sprites.</span><span class="sxs-lookup"><span data-stu-id="5462f-104">Set the view transform that applies to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="5462f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5462f-105">Syntax</span></span>


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a><span data-ttu-id="5462f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5462f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5462f-107">*pViewTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5462f-107">*pViewTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5462f-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="5462f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5462f-109">Pointeur vers un D3DXMATRIX qui contient une transformation du sprite à partir de l’espace universel d’origine.</span><span class="sxs-lookup"><span data-stu-id="5462f-109">Pointer to a D3DXMATRIX that contains a transform of the sprite from the original world space.</span></span> <span data-ttu-id="5462f-110">Utilisez cette transformation pour mettre à l’échelle, faire pivoter ou transformer le sprite.</span><span class="sxs-lookup"><span data-stu-id="5462f-110">Use this transform to scale, rotate, or transform the sprite.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5462f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5462f-111">Return value</span></span>

<span data-ttu-id="5462f-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5462f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5462f-113">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5462f-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5462f-114">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5462f-114">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5462f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5462f-115">Requirements</span></span>



| <span data-ttu-id="5462f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5462f-116">Requirement</span></span> | <span data-ttu-id="5462f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5462f-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5462f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="5462f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5462f-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5462f-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5462f-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5462f-120">Library</span></span><br/> | <dl> <span data-ttu-id="5462f-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5462f-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5462f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5462f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5462f-123">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="5462f-123">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="5462f-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="5462f-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
