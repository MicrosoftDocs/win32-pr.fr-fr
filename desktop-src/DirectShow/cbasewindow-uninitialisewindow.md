---
description: La méthode UninitialiseWindow libère les ressources de la fenêtre.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Méthode CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545679"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="bee7e-103">Méthode CBaseWindow. UninitialiseWindow</span><span class="sxs-lookup"><span data-stu-id="bee7e-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="bee7e-104">La `UninitialiseWindow` méthode libère les ressources de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bee7e-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bee7e-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="bee7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bee7e-106">Parameters</span></span>

<span data-ttu-id="bee7e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bee7e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bee7e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bee7e-108">Return value</span></span>

<span data-ttu-id="bee7e-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bee7e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bee7e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bee7e-110">Remarks</span></span>

<span data-ttu-id="bee7e-111">Cette méthode libère les ressources acquises par la méthode [**CBaseWindow :: InitialiseWindow**](cbasewindow-initialisewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="bee7e-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="bee7e-112">La méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bee7e-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bee7e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bee7e-113">Requirements</span></span>



| <span data-ttu-id="bee7e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bee7e-114">Requirement</span></span> | <span data-ttu-id="bee7e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bee7e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee7e-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="bee7e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bee7e-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bee7e-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bee7e-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bee7e-118">Library</span></span><br/> | <dl> <span data-ttu-id="bee7e-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bee7e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bee7e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee7e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bee7e-121">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="bee7e-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




