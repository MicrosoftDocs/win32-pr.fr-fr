---
description: Anime le maillage et avance l’heure de l’animation globale d’une valeur spécifiée.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController :: AdvanceTime, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535838"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a><span data-ttu-id="45525-103">ID3DXAnimationController :: AdvanceTime, méthode</span><span class="sxs-lookup"><span data-stu-id="45525-103">ID3DXAnimationController::AdvanceTime method</span></span>

<span data-ttu-id="45525-104">Anime le maillage et avance l’heure de l’animation globale d’une valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="45525-104">Animates the mesh and advances the global animation time by a specified amount.</span></span>

## <a name="syntax"></a><span data-ttu-id="45525-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45525-105">Syntax</span></span>


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a><span data-ttu-id="45525-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45525-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45525-107">*TimeDelta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45525-107">*TimeDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45525-108">Type : **[ **double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45525-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45525-109">Durée, en secondes, d’avancement de l’animation globale.</span><span class="sxs-lookup"><span data-stu-id="45525-109">Amount, in seconds, by which to advance the global animation time.</span></span> <span data-ttu-id="45525-110">La valeur TimeDelta doit être non négative ou zéro.</span><span class="sxs-lookup"><span data-stu-id="45525-110">TimeDelta value must be non-negative or zero.</span></span>

</dd> <dt>

<span data-ttu-id="45525-111">*pCallbackHandler* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45525-111">*pCallbackHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45525-112">Type : **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span><span class="sxs-lookup"><span data-stu-id="45525-112">Type: **[**LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**</span></span>

<span data-ttu-id="45525-113">Pointeur vers une interface de gestionnaire de rappel d’animation définie par l’utilisateur, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span><span class="sxs-lookup"><span data-stu-id="45525-113">Pointer to a user-defined animation callback handler interface, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45525-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45525-114">Return value</span></span>

<span data-ttu-id="45525-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45525-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45525-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45525-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="45525-117">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="45525-117">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="45525-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45525-118">Requirements</span></span>



| <span data-ttu-id="45525-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45525-119">Requirement</span></span> | <span data-ttu-id="45525-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="45525-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45525-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="45525-121">Header</span></span><br/>  | <dl> <span data-ttu-id="45525-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="45525-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="45525-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="45525-123">Library</span></span><br/> | <dl> <span data-ttu-id="45525-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45525-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45525-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45525-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45525-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="45525-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
