---
description: Message privé qui amène la fenêtre au premier plan.
ms.assetid: 88b28888-d729-4cf3-8b9d-618dbe150926
title: 'Membre CBaseWindow :: m_ShowStageMessage (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageMessage
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ccf358eba577c0ee950f8628090a2f3024297fe3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532199"
---
# <a name="cbasewindowm_showstagemessage-member"></a><span data-ttu-id="b7d5d-103">CBaseWindow :: m \_ ShowStageMessage, membre</span><span class="sxs-lookup"><span data-stu-id="b7d5d-103">CBaseWindow::m\_ShowStageMessage member</span></span>

<span data-ttu-id="b7d5d-104">Message privé qui amène la fenêtre au premier plan.</span><span class="sxs-lookup"><span data-stu-id="b7d5d-104">Private message that brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7d5d-105">Syntax</span></span>


```C++
UINT m_ShowStageMessage;
```



## <a name="remarks"></a><span data-ttu-id="b7d5d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b7d5d-106">Remarks</span></span>

<span data-ttu-id="b7d5d-107">La méthode [**CBaseWindow ::D osetwindowforeground**](cbasewindow-dosetwindowforeground.md) envoie ce message.</span><span class="sxs-lookup"><span data-stu-id="b7d5d-107">The [**CBaseWindow::DoSetWindowForeground**](cbasewindow-dosetwindowforeground.md) method sends this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d5d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7d5d-108">Requirements</span></span>



| <span data-ttu-id="b7d5d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7d5d-109">Requirement</span></span> | <span data-ttu-id="b7d5d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7d5d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d5d-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7d5d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d5d-112"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7d5d-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7d5d-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7d5d-113">Library</span></span><br/> | <dl> <span data-ttu-id="b7d5d-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7d5d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d5d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7d5d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d5d-116">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="b7d5d-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




