---
description: Ajoute une animation définie au contrôleur d’animation.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'ID3DXAnimationController :: RegisterAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529627"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a><span data-ttu-id="f88cb-103">ID3DXAnimationController :: RegisterAnimationSet, méthode</span><span class="sxs-lookup"><span data-stu-id="f88cb-103">ID3DXAnimationController::RegisterAnimationSet method</span></span>

<span data-ttu-id="f88cb-104">Ajoute une animation définie au contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="f88cb-104">Adds an animation set to the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="f88cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f88cb-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="f88cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f88cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f88cb-107">*pAnimSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f88cb-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f88cb-108">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="f88cb-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="f88cb-109">Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie à ajouter.</span><span class="sxs-lookup"><span data-stu-id="f88cb-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f88cb-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f88cb-110">Return value</span></span>

<span data-ttu-id="f88cb-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f88cb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f88cb-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f88cb-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f88cb-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f88cb-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f88cb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f88cb-114">Requirements</span></span>



| <span data-ttu-id="f88cb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f88cb-115">Requirement</span></span> | <span data-ttu-id="f88cb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f88cb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f88cb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f88cb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f88cb-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f88cb-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f88cb-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f88cb-119">Library</span></span><br/> | <dl> <span data-ttu-id="f88cb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f88cb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f88cb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f88cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f88cb-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f88cb-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




