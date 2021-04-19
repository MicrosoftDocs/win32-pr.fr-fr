---
description: La méthode PerformanceAlignWindow aligne la position de la fenêtre sur les limites DWORD, pour des performances maximales.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Méthode CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542750"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="33a24-103">Méthode CBaseWindow. PerformanceAlignWindow</span><span class="sxs-lookup"><span data-stu-id="33a24-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="33a24-104">La `PerformanceAlignWindow` méthode aligne la position de la fenêtre sur les limites **DWORD** , pour des performances maximales.</span><span class="sxs-lookup"><span data-stu-id="33a24-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33a24-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="33a24-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33a24-106">Parameters</span></span>

<span data-ttu-id="33a24-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="33a24-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33a24-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33a24-108">Return value</span></span>

<span data-ttu-id="33a24-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33a24-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="33a24-110">Notes</span><span class="sxs-lookup"><span data-stu-id="33a24-110">Remarks</span></span>

<span data-ttu-id="33a24-111">Cette méthode aligne les bords gauche et supérieur de la fenêtre sur les limites DWORD, ce qui peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="33a24-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="33a24-112">Si la fenêtre a un parent, la méthode retourne S \_ OK, mais effectue l’alignement.</span><span class="sxs-lookup"><span data-stu-id="33a24-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a24-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33a24-113">Requirements</span></span>



| <span data-ttu-id="33a24-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33a24-114">Requirement</span></span> | <span data-ttu-id="33a24-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="33a24-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a24-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="33a24-116">Header</span></span><br/>  | <dl> <span data-ttu-id="33a24-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33a24-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33a24-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33a24-118">Library</span></span><br/> | <dl> <span data-ttu-id="33a24-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="33a24-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a24-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33a24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a24-121">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="33a24-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




