---
description: La \_ méthode put WindowState définit l’état de la fenêtre.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Méthode CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521763"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a><span data-ttu-id="e4ad6-103">Méthode CBaseControlWindow. put \_ WindowState</span><span class="sxs-lookup"><span data-stu-id="e4ad6-103">CBaseControlWindow.put\_WindowState method</span></span>

<span data-ttu-id="e4ad6-104">La `put_WindowState` méthode définit l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-104">The `put_WindowState` method sets the window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ad6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4ad6-105">Syntax</span></span>


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a><span data-ttu-id="e4ad6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4ad6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ad6-107">*WindowState*</span><span class="sxs-lookup"><span data-stu-id="e4ad6-107">*WindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="e4ad6-108">Nouvel état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e4ad6-108">New window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ad6-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4ad6-109">Return value</span></span>

<span data-ttu-id="e4ad6-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4ad6-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ad6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e4ad6-111">Remarks</span></span>

<span data-ttu-id="e4ad6-112">Cette fonction membre accepte les mêmes paramètres que la fonction Microsoft Win32 **ShowWindow** (par exemple, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE et WS \_ SHOWMAXIMIZED).</span><span class="sxs-lookup"><span data-stu-id="e4ad6-112">This member function takes the same parameters as the Microsoft Win32 **ShowWindow** function (for example, WS\_SHOWNORMAL, WS\_SHOWMINNOACTIVATE, and WS\_SHOWMAXIMIZED).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ad6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4ad6-113">Requirements</span></span>



| <span data-ttu-id="e4ad6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4ad6-114">Requirement</span></span> | <span data-ttu-id="e4ad6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4ad6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ad6-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4ad6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e4ad6-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ad6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4ad6-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4ad6-118">Library</span></span><br/> | <dl> <span data-ttu-id="e4ad6-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ad6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ad6-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ad6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ad6-121">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="e4ad6-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




