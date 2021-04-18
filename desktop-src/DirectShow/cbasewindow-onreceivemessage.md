---
description: La méthode OnReceiveMessage gère les messages de fenêtre.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Méthode CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540361"
---
# <a name="cbasewindowonreceivemessage-method"></a><span data-ttu-id="6cb19-103">Méthode CBaseWindow. OnReceiveMessage</span><span class="sxs-lookup"><span data-stu-id="6cb19-103">CBaseWindow.OnReceiveMessage method</span></span>

<span data-ttu-id="6cb19-104">La `OnReceiveMessage` méthode gère les messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6cb19-104">The `OnReceiveMessage` method handles window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cb19-105">Syntax</span></span>


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="6cb19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cb19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb19-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6cb19-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb19-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6cb19-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="6cb19-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="6cb19-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb19-110">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="6cb19-110">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6cb19-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cb19-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb19-112">Premier paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="6cb19-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6cb19-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cb19-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cb19-114">Deuxième paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="6cb19-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb19-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cb19-115">Return value</span></span>

<span data-ttu-id="6cb19-116">Retourne 0 si le message a été traité, ou 1 si le message n’a pas été traité.</span><span class="sxs-lookup"><span data-stu-id="6cb19-116">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb19-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6cb19-117">Remarks</span></span>

<span data-ttu-id="6cb19-118">La classe de base gère les messages suivants :</span><span class="sxs-lookup"><span data-stu-id="6cb19-118">The base class handles the following messages:</span></span>

-   <span data-ttu-id="6cb19-119">\_Fermer WM</span><span class="sxs-lookup"><span data-stu-id="6cb19-119">WM\_CLOSE</span></span>
-   <span data-ttu-id="6cb19-120">déplacement de WM \_</span><span class="sxs-lookup"><span data-stu-id="6cb19-120">WM\_MOVE</span></span>
-   <span data-ttu-id="6cb19-121">\_PALETTECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="6cb19-121">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="6cb19-122">\_QUERYNEWPALETTE WM</span><span class="sxs-lookup"><span data-stu-id="6cb19-122">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="6cb19-123">taille du WM \_</span><span class="sxs-lookup"><span data-stu-id="6cb19-123">WM\_SIZE</span></span>
-   <span data-ttu-id="6cb19-124">\_SYSCOLORCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="6cb19-124">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="6cb19-125">Une classe dérivée peut substituer cette méthode pour gérer d’autres messages.</span><span class="sxs-lookup"><span data-stu-id="6cb19-125">A derived class can override this method to handle other messages.</span></span> <span data-ttu-id="6cb19-126">La classe dérivée doit appeler la méthode de la classe de base pour gérer tous les messages ignorés par la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="6cb19-126">The derived class should call the base class method to handle any messages that the derived class ignores.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb19-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cb19-127">Requirements</span></span>



| <span data-ttu-id="6cb19-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cb19-128">Requirement</span></span> | <span data-ttu-id="6cb19-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cb19-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb19-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cb19-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6cb19-131"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb19-131"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6cb19-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cb19-132">Library</span></span><br/> | <dl> <span data-ttu-id="6cb19-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb19-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb19-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cb19-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb19-135">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="6cb19-135">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




