---
description: La \_ méthode put WindowStyleEx définit les styles de fenêtre étendus.
ms.assetid: 3c5928fe-7cd3-4e1c-9a3f-fa6d7a73dbc3
title: Méthode CBaseControlWindow.put_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ee04cf2d2b2dcaafdaf4e989fd1118abf447698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537906"
---
# <a name="cbasecontrolwindowput_windowstyleex-method"></a><span data-ttu-id="7d0d1-103">CBaseControlWindow. put \_ WindowStyleEx, méthode</span><span class="sxs-lookup"><span data-stu-id="7d0d1-103">CBaseControlWindow.put\_WindowStyleEx method</span></span>

<span data-ttu-id="7d0d1-104">La `put_WindowStyleEx` méthode définit les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-104">The `put_WindowStyleEx` method sets the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0d1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d0d1-105">Syntax</span></span>


```C++
HRESULT put_WindowStyleEx(
  [in] long WindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="7d0d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d0d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d0d1-107">*WindowStyleEx* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d0d1-107">*WindowStyleEx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d0d1-108">Valeur qui spécifie le style de la fenêtre de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-108">Value that specifies the style of the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d0d1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d0d1-109">Return value</span></span>

<span data-ttu-id="7d0d1-110">Retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-110">Returns NOERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0d1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7d0d1-111">Remarks</span></span>

<span data-ttu-id="7d0d1-112">Cette méthode utilise des styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-112">This method uses extended window styles.</span></span> <span data-ttu-id="7d0d1-113">Pour obtenir la liste complète des styles de fenêtre étendus, consultez la fonction Microsoft Win32 **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="7d0d1-113">For a complete list of extended window styles, see the Microsoft Win32 **CreateWindowEx** function.</span></span> <span data-ttu-id="7d0d1-114">Pour modifier le style de la fenêtre, récupérez le style de la fenêtre active, puis ajoutez ou supprimez les champs de bits nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-114">To change the window style, retrieve the current window style, and then add or remove the necessary bit fields.</span></span>

<span data-ttu-id="7d0d1-115">N’utilisez pas les styles de fenêtre suivants, car ils ne sont pas validés.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-115">Do not use the following window styles because they are not validated.</span></span>

-   <span data-ttu-id="7d0d1-116">WS \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="7d0d1-116">WS\_DISABLED</span></span>
-   <span data-ttu-id="7d0d1-117">\_HSCROLL WS</span><span class="sxs-lookup"><span data-stu-id="7d0d1-117">WS\_HSCROLL</span></span>
-   <span data-ttu-id="7d0d1-118">\_sous forme WS</span><span class="sxs-lookup"><span data-stu-id="7d0d1-118">WS\_ICONIC</span></span>
-   <span data-ttu-id="7d0d1-119">\_optimisation WS</span><span class="sxs-lookup"><span data-stu-id="7d0d1-119">WS\_MAXIMIZE</span></span>
-   <span data-ttu-id="7d0d1-120">WS \_ réduire</span><span class="sxs-lookup"><span data-stu-id="7d0d1-120">WS\_MINIMIZE</span></span>
-   <span data-ttu-id="7d0d1-121">\_VSCROLL WS</span><span class="sxs-lookup"><span data-stu-id="7d0d1-121">WS\_VSCROLL</span></span>

<span data-ttu-id="7d0d1-122">À quelques exceptions près (notées ici), les indicateurs acceptables sont les mêmes que ceux autorisés par la fonction **CreateWindow** Win32.</span><span class="sxs-lookup"><span data-stu-id="7d0d1-122">With some exceptions (noted here), the acceptable flags are the same as those allowed by the Win32 **CreateWindow** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d0d1-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d0d1-123">Requirements</span></span>



| <span data-ttu-id="7d0d1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d0d1-124">Requirement</span></span> | <span data-ttu-id="7d0d1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d0d1-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0d1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d0d1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7d0d1-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d0d1-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7d0d1-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7d0d1-128">Library</span></span><br/> | <dl> <span data-ttu-id="7d0d1-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7d0d1-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d0d1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d0d1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0d1-131">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="7d0d1-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




