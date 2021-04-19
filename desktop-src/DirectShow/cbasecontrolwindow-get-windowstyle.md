---
description: La \_ méthode obtenir WindowStyle récupère les styles de fenêtre standard.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Méthode CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542739"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="7e448-103">CBaseControlWindow. obten, \_ méthode WindowStyle</span><span class="sxs-lookup"><span data-stu-id="7e448-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="7e448-104">La `get_WindowStyle` méthode récupère les styles de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="7e448-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e448-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e448-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="7e448-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e448-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e448-107">*pWindowStyle*</span><span class="sxs-lookup"><span data-stu-id="7e448-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="7e448-108">Pointeur vers les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7e448-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e448-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e448-109">Return value</span></span>

<span data-ttu-id="7e448-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e448-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e448-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7e448-111">Remarks</span></span>

<span data-ttu-id="7e448-112">Cette fonction membre retourne les styles de fenêtre standard, tels que WS \_ Child et WS \_ visible.</span><span class="sxs-lookup"><span data-stu-id="7e448-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="7e448-113">Elle appelle la fonction membre [**CBaseControlWindow ::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="7e448-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e448-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e448-114">Requirements</span></span>



| <span data-ttu-id="7e448-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e448-115">Requirement</span></span> | <span data-ttu-id="7e448-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e448-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e448-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e448-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7e448-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e448-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7e448-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e448-119">Library</span></span><br/> | <dl> <span data-ttu-id="7e448-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7e448-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e448-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e448-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e448-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="7e448-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




