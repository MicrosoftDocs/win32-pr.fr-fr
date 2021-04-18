---
description: La méthode PossiblyEatMessage permet à une classe dérivée de transférer des messages à une autre fenêtre.
ms.assetid: d8775182-44ed-4df2-b4b8-1fdf289e2c1a
title: Méthode CBaseWindow. PossiblyEatMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PossiblyEatMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f218b62ac5464da27b8596992c34ce7ae5efde46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532968"
---
# <a name="cbasewindowpossiblyeatmessage-method"></a><span data-ttu-id="0c822-103">Méthode CBaseWindow. PossiblyEatMessage</span><span class="sxs-lookup"><span data-stu-id="0c822-103">CBaseWindow.PossiblyEatMessage method</span></span>

<span data-ttu-id="0c822-104">La `PossiblyEatMessage` méthode permet à une classe dérivée de transférer des messages à une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0c822-104">The `PossiblyEatMessage` method enables a derived class to forward messages to another window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c822-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c822-105">Syntax</span></span>


```C++
virtual BOOL PossiblyEatMessage(
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="0c822-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c822-107">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="0c822-107">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="0c822-108">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="0c822-108">Message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0c822-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c822-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c822-110">Premier paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="0c822-110">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0c822-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c822-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c822-112">Deuxième paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="0c822-112">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c822-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c822-113">Return value</span></span>

<span data-ttu-id="0c822-114">Retourne la **valeur true** si le message a été transféré, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0c822-114">Returns **TRUE** if the message was forwarded, or **FALSE** otherwise.</span></span> <span data-ttu-id="0c822-115">La classe de base retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="0c822-115">The base class returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c822-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0c822-116">Remarks</span></span>

<span data-ttu-id="0c822-117">Avant que la méthode [**CBaseWindow :: OnReceiveMessage**](cbasewindow-onreceivemessage.md) gère un message, elle appelle `PossiblyEatMessage` .</span><span class="sxs-lookup"><span data-stu-id="0c822-117">Before the [**CBaseWindow::OnReceiveMessage**](cbasewindow-onreceivemessage.md) method handles a message, it calls `PossiblyEatMessage`.</span></span> <span data-ttu-id="0c822-118">Si `PossiblyEatMessage` retourne **true**, **OnReceiveMessage** ignore le message.</span><span class="sxs-lookup"><span data-stu-id="0c822-118">If `PossiblyEatMessage` returns **TRUE**, **OnReceiveMessage** ignores the message.</span></span> <span data-ttu-id="0c822-119">Une classe dérivée peut être substituée `PossiblyEatMessage` afin de transférer des messages à une fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="0c822-119">A derived class can override `PossiblyEatMessage` so that it forwards some messages to an owner window.</span></span> <span data-ttu-id="0c822-120">Par exemple, la classe [**CBaseControlWindow**](cbasecontrolwindow.md) , qui dérive de **CBaseWindow**, transfère les messages de clavier et de souris.</span><span class="sxs-lookup"><span data-stu-id="0c822-120">For example, the [**CBaseControlWindow**](cbasecontrolwindow.md) class, which derives from **CBaseWindow**, forwards keyboard and mouse messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c822-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c822-121">Requirements</span></span>



| <span data-ttu-id="0c822-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c822-122">Requirement</span></span> | <span data-ttu-id="0c822-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c822-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c822-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c822-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0c822-125"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c822-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c822-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c822-126">Library</span></span><br/> | <dl> <span data-ttu-id="0c822-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0c822-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c822-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c822-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c822-129">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="0c822-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




