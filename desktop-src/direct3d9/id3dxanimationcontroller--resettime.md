---
description: Réinitialise l’heure de l’animation globale à zéro. Tous les événements en attente conservent leurs planifications d’origine, mais dans le nouveau délai.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController :: ResetTime, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762211"
---
# <a name="id3dxanimationcontrollerresettime-method"></a><span data-ttu-id="f31e2-104">ID3DXAnimationController :: ResetTime, méthode</span><span class="sxs-lookup"><span data-stu-id="f31e2-104">ID3DXAnimationController::ResetTime method</span></span>

<span data-ttu-id="f31e2-105">Réinitialise l’heure de l’animation globale à zéro.</span><span class="sxs-lookup"><span data-stu-id="f31e2-105">Resets the global animation time to zero.</span></span> <span data-ttu-id="f31e2-106">Tous les événements en attente conservent leurs planifications d’origine, mais dans le nouveau délai.</span><span class="sxs-lookup"><span data-stu-id="f31e2-106">Any pending events will retain their original schedules, but in the new timeframe.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31e2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f31e2-107">Syntax</span></span>


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a><span data-ttu-id="f31e2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f31e2-108">Parameters</span></span>

<span data-ttu-id="f31e2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f31e2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31e2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f31e2-110">Return value</span></span>

<span data-ttu-id="f31e2-111">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f31e2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f31e2-112">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f31e2-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f31e2-113">Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f31e2-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31e2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f31e2-114">Remarks</span></span>

<span data-ttu-id="f31e2-115">Cette méthode est généralement utilisée lorsque la valeur d’heure de l’animation globale est proche de la précision maximale du DOUBLE stockage, ou 2 ⁶ ⁴-1.</span><span class="sxs-lookup"><span data-stu-id="f31e2-115">This method is typically used when the global animation time value is nearing the maximum precision of DOUBLE storage, or 2⁶⁴ - 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31e2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f31e2-116">Requirements</span></span>



| <span data-ttu-id="f31e2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f31e2-117">Requirement</span></span> | <span data-ttu-id="f31e2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f31e2-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31e2-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="f31e2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f31e2-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f31e2-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f31e2-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f31e2-121">Library</span></span><br/> | <dl> <span data-ttu-id="f31e2-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f31e2-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f31e2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f31e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31e2-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f31e2-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




