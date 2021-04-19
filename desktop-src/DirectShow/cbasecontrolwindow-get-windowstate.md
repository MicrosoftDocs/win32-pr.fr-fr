---
description: La \_ méthode obtenir WindowState récupère l’état actuel de la fenêtre.
ms.assetid: 118b6710-b041-4a7d-8cdb-b96ae3dcbb09
title: Méthode CBaseControlWindow.get_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5391a118e2ae860a37905c7ff94822ad7c422135
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541721"
---
# <a name="cbasecontrolwindowget_windowstate-method"></a><span data-ttu-id="be4a8-103">CBaseControlWindow. obten, \_ méthode WindowState</span><span class="sxs-lookup"><span data-stu-id="be4a8-103">CBaseControlWindow.get\_WindowState method</span></span>

<span data-ttu-id="be4a8-104">La `get_WindowState` méthode récupère l’état actuel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be4a8-104">The `get_WindowState` method retrieves the current window state.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be4a8-105">Syntax</span></span>


```C++
HRESULT get_WindowState(
   long *pWindowState
);
```



## <a name="parameters"></a><span data-ttu-id="be4a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be4a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be4a8-107">*pWindowState*</span><span class="sxs-lookup"><span data-stu-id="be4a8-107">*pWindowState*</span></span> 
</dt> <dd>

<span data-ttu-id="be4a8-108">Pointeur vers l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be4a8-108">Pointer to the window state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be4a8-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be4a8-109">Return value</span></span>

<span data-ttu-id="be4a8-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be4a8-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be4a8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="be4a8-111">Remarks</span></span>

<span data-ttu-id="be4a8-112">Cette fonction membre retourne un sous-ensemble des paramètres de la fonction Microsoft Win32 **ShowWindow** .</span><span class="sxs-lookup"><span data-stu-id="be4a8-112">This member function returns a subset of the parameters of the Microsoft Win32 **ShowWindow** function.</span></span> <span data-ttu-id="be4a8-113">En particulier, elle retourne l' \_ affichage logiciel et le \_ masquage logiciel, selon la visibilité actuelle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="be4a8-113">In particular, it returns SW\_SHOW and SW\_HIDE, depending on the current visibility of the window.</span></span> <span data-ttu-id="be4a8-114">Il retourne également \_ les logiciels Minimize et \_ maximiser, selon que la fenêtre est une icône ou qu’elle est développée.</span><span class="sxs-lookup"><span data-stu-id="be4a8-114">It also returns SW\_MINIMIZE and SW\_MAXIMIZE, depending on whether the window is an icon or is expanded.</span></span>

## <a name="requirements"></a><span data-ttu-id="be4a8-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be4a8-115">Requirements</span></span>



| <span data-ttu-id="be4a8-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be4a8-116">Requirement</span></span> | <span data-ttu-id="be4a8-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="be4a8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be4a8-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="be4a8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="be4a8-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be4a8-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be4a8-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be4a8-120">Library</span></span><br/> | <dl> <span data-ttu-id="be4a8-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be4a8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4a8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4a8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4a8-123">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="be4a8-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




