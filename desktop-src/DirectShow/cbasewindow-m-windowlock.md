---
description: Section critique, pour sérialiser l’accès à l’objet.
ms.assetid: 24a5b1b2-209e-4262-aa48-fd4534b2da57
title: 'Membre CBaseWindow :: m_WindowLock (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WindowLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38227e505f2e05e024c8cecf12ab3cb8c336bfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540207"
---
# <a name="cbasewindowm_windowlock-member"></a><span data-ttu-id="5cf39-103">CBaseWindow :: m \_ WindowLock, membre</span><span class="sxs-lookup"><span data-stu-id="5cf39-103">CBaseWindow::m\_WindowLock member</span></span>

<span data-ttu-id="5cf39-104">Section critique, pour sérialiser l’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="5cf39-104">Critical section, to serialize access to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cf39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cf39-105">Syntax</span></span>


```C++
CCritSec m_WindowLock;
```



## <a name="requirements"></a><span data-ttu-id="5cf39-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cf39-106">Requirements</span></span>



| <span data-ttu-id="5cf39-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cf39-107">Requirement</span></span> | <span data-ttu-id="5cf39-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cf39-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf39-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cf39-109">Header</span></span><br/>  | <dl> <span data-ttu-id="5cf39-110"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf39-110"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5cf39-111">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5cf39-111">Library</span></span><br/> | <dl> <span data-ttu-id="5cf39-112"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5cf39-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf39-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf39-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf39-114">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="5cf39-114">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




