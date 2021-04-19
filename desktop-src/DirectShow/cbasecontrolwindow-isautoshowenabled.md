---
description: La méthode IsAutoShowEnabled récupère des informations indiquant si la fenêtre vidéo s’affiche automatiquement lorsque le filtre de rendu s’interrompt ou s’exécute.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Méthode CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532671"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="805d2-103">Méthode CBaseControlWindow. IsAutoShowEnabled</span><span class="sxs-lookup"><span data-stu-id="805d2-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="805d2-104">La `IsAutoShowEnabled` méthode récupère des informations indiquant si la fenêtre vidéo s’affiche automatiquement lorsque le filtre de rendu s’interrompt ou s’exécute.</span><span class="sxs-lookup"><span data-stu-id="805d2-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="805d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="805d2-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="805d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="805d2-106">Parameters</span></span>

<span data-ttu-id="805d2-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="805d2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="805d2-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="805d2-108">Return value</span></span>

<span data-ttu-id="805d2-109">Retourne la **valeur true** si le membre **m \_ bAutoShow** a la valeur 1 ou **false** s’il a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="805d2-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="805d2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="805d2-110">Remarks</span></span>

<span data-ttu-id="805d2-111">Si le membre **m \_ bAutoShow** a la valeur 1 dans une fenêtre vidéo masquée, la fenêtre devient visible lorsque le filtre s’interrompt ou s’exécute.</span><span class="sxs-lookup"><span data-stu-id="805d2-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="805d2-112">Si ce membre a la valeur 0, la fenêtre s’affiche uniquement si vous utilisez la fonction membre [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="805d2-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="805d2-113">Cette fonction membre récupère le paramètre de membre **m \_ bAutoShow** et produit le même résultat que l’utilisation de la méthode [**IVideoWindow :: obtenir \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="805d2-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="805d2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="805d2-114">Requirements</span></span>



| <span data-ttu-id="805d2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="805d2-115">Requirement</span></span> | <span data-ttu-id="805d2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="805d2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805d2-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="805d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="805d2-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="805d2-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="805d2-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="805d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="805d2-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="805d2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805d2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="805d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805d2-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="805d2-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




