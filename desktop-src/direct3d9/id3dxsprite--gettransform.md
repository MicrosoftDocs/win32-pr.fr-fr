---
description: Obtient la transformation de sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'ID3DXSprite :: GetTransform, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043124"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="58ff0-103">ID3DXSprite :: GetTransform, méthode</span><span class="sxs-lookup"><span data-stu-id="58ff0-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="58ff0-104">Obtient la transformation de sprite.</span><span class="sxs-lookup"><span data-stu-id="58ff0-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ff0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58ff0-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="58ff0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58ff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ff0-107">*pTransform* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="58ff0-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ff0-108">Type : **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="58ff0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="58ff0-109">Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation du sprite à partir de l’espace universel d’origine.</span><span class="sxs-lookup"><span data-stu-id="58ff0-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ff0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="58ff0-110">Return value</span></span>

<span data-ttu-id="58ff0-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58ff0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58ff0-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58ff0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="58ff0-113">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="58ff0-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="58ff0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ff0-114">Requirements</span></span>



| <span data-ttu-id="58ff0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ff0-115">Requirement</span></span> | <span data-ttu-id="58ff0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ff0-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58ff0-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="58ff0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="58ff0-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ff0-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="58ff0-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58ff0-119">Library</span></span><br/> | <dl> <span data-ttu-id="58ff0-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ff0-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58ff0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ff0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ff0-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="58ff0-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




