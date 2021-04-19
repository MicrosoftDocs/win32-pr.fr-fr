---
description: La méthode NotifyOwnerMessage transmet des messages spécifiques à la fenêtre vidéo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Méthode CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530038"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a><span data-ttu-id="ca95a-103">Méthode CBaseControlWindow. NotifyOwnerMessage</span><span class="sxs-lookup"><span data-stu-id="ca95a-103">CBaseControlWindow.NotifyOwnerMessage method</span></span>

<span data-ttu-id="ca95a-104">La `NotifyOwnerMessage` méthode passe sur des messages spécifiques à la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca95a-104">The `NotifyOwnerMessage` method passes along specific messages to the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca95a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca95a-105">Syntax</span></span>


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ca95a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca95a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca95a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ca95a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ca95a-108">Handle vers la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca95a-108">Handle to the video window.</span></span>

</dd> <dt>

<span data-ttu-id="ca95a-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="ca95a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ca95a-110">Détails du message.</span><span class="sxs-lookup"><span data-stu-id="ca95a-110">Message details.</span></span>

</dd> <dt>

<span data-ttu-id="ca95a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca95a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca95a-112">Premier paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="ca95a-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ca95a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca95a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca95a-114">Deuxième paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="ca95a-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca95a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca95a-115">Return value</span></span>

<span data-ttu-id="ca95a-116">Ne retourne aucune \_ erreur.</span><span class="sxs-lookup"><span data-stu-id="ca95a-116">Returns NO\_ERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca95a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ca95a-117">Remarks</span></span>

<span data-ttu-id="ca95a-118">Quand la fenêtre vidéo est un enfant d’une autre fenêtre, elle ne reçoit pas certains messages de la fenêtre de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ca95a-118">When the video window is a child of another window, it does not receive certain top-level window messages.</span></span> <span data-ttu-id="ca95a-119">Ces messages peuvent être utiles à un convertisseur, car ils peuvent affecter son comportement.</span><span class="sxs-lookup"><span data-stu-id="ca95a-119">These messages can be valuable to a renderer, because they could affect its behavior.</span></span> <span data-ttu-id="ca95a-120">`NotifyOwnerMessage` passe l’un des messages suivants à la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="ca95a-120">`NotifyOwnerMessage` passes any of the following messages to the video window.</span></span>

-   <span data-ttu-id="ca95a-121">\_ACTIVATEAPP WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-121">WM\_ACTIVATEAPP</span></span>
-   <span data-ttu-id="ca95a-122">\_DEVMODECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-122">WM\_DEVMODECHANGE</span></span>
-   <span data-ttu-id="ca95a-123">\_DISPLAYCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-123">WM\_DISPLAYCHANGE</span></span>
-   <span data-ttu-id="ca95a-124">\_PALETTECHANGED WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-124">WM\_PALETTECHANGED</span></span>
-   <span data-ttu-id="ca95a-125">\_PALETTEISCHANGING WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-125">WM\_PALETTEISCHANGING</span></span>
-   <span data-ttu-id="ca95a-126">\_QUERYNEWPALETTE WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-126">WM\_QUERYNEWPALETTE</span></span>
-   <span data-ttu-id="ca95a-127">\_SYSCOLORCHANGE WM</span><span class="sxs-lookup"><span data-stu-id="ca95a-127">WM\_SYSCOLORCHANGE</span></span>

<span data-ttu-id="ca95a-128">Vous pouvez demander à ce que le serveur de distribution de plug-ins [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) devienne l’enfant d’une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ca95a-128">You can request that the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor (PID) make a window become a child of another window.</span></span> <span data-ttu-id="ca95a-129">Dans ce cas, le PID recherche certains messages qui peuvent être envoyés à la fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ca95a-129">When this occurs, the PID will look for certain messages that might be sent to the owning window.</span></span> <span data-ttu-id="ca95a-130">Le PID transmet ensuite ces messages à la fenêtre qui en est propriétaire.</span><span class="sxs-lookup"><span data-stu-id="ca95a-130">The PID will then forward those messages to the owned window.</span></span> <span data-ttu-id="ca95a-131">Le traitement par défaut des messages consiste à les envoyer de façon synchrone à la procédure de fenêtre appartenant en appelant la fonction Win32 **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="ca95a-131">The default processing for the messages is to send them to the owned window procedure synchronously by calling the Win32 **SendMessage** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca95a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca95a-132">Requirements</span></span>



| <span data-ttu-id="ca95a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca95a-133">Requirement</span></span> | <span data-ttu-id="ca95a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca95a-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca95a-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca95a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="ca95a-136"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca95a-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca95a-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca95a-137">Library</span></span><br/> | <dl> <span data-ttu-id="ca95a-138"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ca95a-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca95a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca95a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca95a-140">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="ca95a-140">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




