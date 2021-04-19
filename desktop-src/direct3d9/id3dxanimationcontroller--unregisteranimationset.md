---
description: Supprime un jeu d’animations du contrôleur d’animation.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'ID3DXAnimationController :: UnregisterAnimationSet, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532691"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a><span data-ttu-id="4fa40-103">ID3DXAnimationController :: UnregisterAnimationSet, méthode</span><span class="sxs-lookup"><span data-stu-id="4fa40-103">ID3DXAnimationController::UnregisterAnimationSet method</span></span>

<span data-ttu-id="4fa40-104">Supprime un jeu d’animations du contrôleur d’animation.</span><span class="sxs-lookup"><span data-stu-id="4fa40-104">Removes an animation set from the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa40-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fa40-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="4fa40-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fa40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa40-107">*pAnimSet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4fa40-107">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa40-108">Type : **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="4fa40-108">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="4fa40-109">Pointeur vers l’animation [**ID3DXAnimationSet**](id3dxanimationset.md) définie sur supprimer.</span><span class="sxs-lookup"><span data-stu-id="4fa40-109">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa40-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4fa40-110">Return value</span></span>

<span data-ttu-id="4fa40-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4fa40-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4fa40-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4fa40-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4fa40-113">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="4fa40-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa40-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fa40-114">Requirements</span></span>



| <span data-ttu-id="4fa40-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fa40-115">Requirement</span></span> | <span data-ttu-id="4fa40-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fa40-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa40-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="4fa40-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4fa40-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa40-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4fa40-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4fa40-119">Library</span></span><br/> | <dl> <span data-ttu-id="4fa40-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fa40-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fa40-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fa40-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa40-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="4fa40-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




