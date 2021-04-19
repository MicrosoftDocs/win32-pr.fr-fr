---
description: Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membre CBaseWindow :: m_ShowStageTop (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542259"
---
# <a name="cbasewindowm_showstagetop-member"></a><span data-ttu-id="9ceed-103">CBaseWindow :: m \_ ShowStageTop, membre</span><span class="sxs-lookup"><span data-stu-id="9ceed-103">CBaseWindow::m\_ShowStageTop member</span></span>

<span data-ttu-id="9ceed-104">Message privé qui définit le style de fenêtre sur WS \_ ex le \_ plus haut.</span><span class="sxs-lookup"><span data-stu-id="9ceed-104">Private message that sets the window style to WS\_EX\_TOPMOST.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ceed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ceed-105">Syntax</span></span>


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a><span data-ttu-id="9ceed-106">Notes</span><span class="sxs-lookup"><span data-stu-id="9ceed-106">Remarks</span></span>

<span data-ttu-id="9ceed-107">Les convertisseurs vidéo doivent envoyer ce message à la fenêtre s’ils basculent en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9ceed-107">Video renderers should send this message to the window if they switch to full-screen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ceed-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ceed-108">Requirements</span></span>



| <span data-ttu-id="9ceed-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ceed-109">Requirement</span></span> | <span data-ttu-id="9ceed-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ceed-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ceed-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ceed-111">Header</span></span><br/>  | <dl> <span data-ttu-id="9ceed-112"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ceed-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ceed-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ceed-113">Library</span></span><br/> | <dl> <span data-ttu-id="9ceed-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9ceed-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ceed-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ceed-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ceed-116">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="9ceed-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




