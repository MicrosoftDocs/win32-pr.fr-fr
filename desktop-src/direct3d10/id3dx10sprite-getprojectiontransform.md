---
description: Obtient la matrice de projection Sprite qui est appliquée à tous les sprites.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'ID3DX10Sprite :: GetProjectionTransform, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762380"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a><span data-ttu-id="0ea9f-103">ID3DX10Sprite :: GetProjectionTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="0ea9f-103">ID3DX10Sprite::GetProjectionTransform method</span></span>

<span data-ttu-id="0ea9f-104">Obtient la matrice de projection Sprite qui est appliquée à tous les sprites.</span><span class="sxs-lookup"><span data-stu-id="0ea9f-104">Get the sprite projection matrix that is applied to all sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea9f-105">Syntax</span></span>


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a><span data-ttu-id="0ea9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ea9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea9f-107">*pProjectionTransform* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ea9f-107">*pProjectionTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea9f-108">Type : **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ea9f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0ea9f-109">Pointeur vers un [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) qui sera défini sur la matrice de projection du sprite.</span><span class="sxs-lookup"><span data-stu-id="0ea9f-109">Pointer to a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) that will be set to the sprite's projection matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea9f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ea9f-110">Return value</span></span>

<span data-ttu-id="0ea9f-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ea9f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ea9f-112">La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0ea9f-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea9f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea9f-113">Requirements</span></span>



| <span data-ttu-id="0ea9f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ea9f-114">Requirement</span></span> | <span data-ttu-id="0ea9f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ea9f-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea9f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ea9f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ea9f-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea9f-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ea9f-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ea9f-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ea9f-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ea9f-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea9f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea9f-121">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="0ea9f-121">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="0ea9f-122">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="0ea9f-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
