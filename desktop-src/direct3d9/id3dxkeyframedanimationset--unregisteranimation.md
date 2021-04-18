---
description: Supprimez les données d’animation du jeu d’animations.
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'ID3DXKeyframedAnimationSet :: UnregisterAnimation, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520348"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="db77e-103">ID3DXKeyframedAnimationSet :: UnregisterAnimation, méthode</span><span class="sxs-lookup"><span data-stu-id="db77e-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="db77e-104">Supprimez les données d’animation du jeu d’animations.</span><span class="sxs-lookup"><span data-stu-id="db77e-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="db77e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db77e-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="db77e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db77e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db77e-107">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db77e-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db77e-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db77e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db77e-109">Index d’animation.</span><span class="sxs-lookup"><span data-stu-id="db77e-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db77e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db77e-110">Return value</span></span>

<span data-ttu-id="db77e-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db77e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db77e-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db77e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="db77e-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="db77e-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="db77e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db77e-114">Requirements</span></span>



| <span data-ttu-id="db77e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db77e-115">Requirement</span></span> | <span data-ttu-id="db77e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="db77e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db77e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="db77e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="db77e-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="db77e-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="db77e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db77e-119">Library</span></span><br/> | <dl> <span data-ttu-id="db77e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db77e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="db77e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db77e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db77e-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="db77e-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
