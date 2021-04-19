---
description: La \_ méthode obtenir MessageDrain récupère le message en cours de drainage.
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: Méthode CBaseControlWindow.get_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542278"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a><span data-ttu-id="ef571-103">Méthode CBaseControlWindow. obten \_ MessageDrain</span><span class="sxs-lookup"><span data-stu-id="ef571-103">CBaseControlWindow.get\_MessageDrain method</span></span>

<span data-ttu-id="ef571-104">La `get_MessageDrain` méthode récupère l’écoulement actuel du message.</span><span class="sxs-lookup"><span data-stu-id="ef571-104">The `get_MessageDrain` method retrieves the current message drain.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef571-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef571-105">Syntax</span></span>


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a><span data-ttu-id="ef571-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef571-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef571-107">*Vidage*</span><span class="sxs-lookup"><span data-stu-id="ef571-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="ef571-108">Pointeur vers la fenêtre active recevant des messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ef571-108">Pointer to the current window receiving window messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef571-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef571-109">Return value</span></span>

<span data-ttu-id="ef571-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef571-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef571-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ef571-111">Remarks</span></span>

<span data-ttu-id="ef571-112">Les messages envoyés au filtre de convertisseur vidéo peuvent être publiés dans une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ef571-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="ef571-113">La fenêtre inscrite pour recevoir ces messages (à l’aide de la fonction membre **CBaseControlWindow :: obtenir \_ MessageDrain** ) est l’drain de message en cours.</span><span class="sxs-lookup"><span data-stu-id="ef571-113">The window registered to receive these messages (using the **CBaseControlWindow::get\_MessageDrain** member function) is the current message drain.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef571-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef571-114">Requirements</span></span>



| <span data-ttu-id="ef571-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef571-115">Requirement</span></span> | <span data-ttu-id="ef571-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef571-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef571-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef571-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ef571-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef571-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef571-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef571-119">Library</span></span><br/> | <dl> <span data-ttu-id="ef571-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef571-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef571-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef571-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef571-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="ef571-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




