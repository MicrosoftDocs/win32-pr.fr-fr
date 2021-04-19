---
description: Indicateur qui spécifie si la fenêtre publie ou envoie son message de destruction.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membre CBaseWindow :: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525548"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="95f18-103">CBaseWindow :: m \_ bDoPostToDestroy, membre</span><span class="sxs-lookup"><span data-stu-id="95f18-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="95f18-104">Indicateur qui spécifie si la fenêtre publie ou envoie son message de destruction.</span><span class="sxs-lookup"><span data-stu-id="95f18-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="95f18-105">Si la **valeur est true**, la méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) utilise la fonction **PostMessage** pour s’envoyer un message de destruction privé.</span><span class="sxs-lookup"><span data-stu-id="95f18-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="95f18-106">Si la **valeur est false**, **DoneWithWindow** utilise la fonction **SendMessage** pour envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="95f18-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="95f18-107">Par défaut, la valeur est **false**.</span><span class="sxs-lookup"><span data-stu-id="95f18-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f18-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95f18-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="95f18-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95f18-109">Requirements</span></span>



| <span data-ttu-id="95f18-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95f18-110">Requirement</span></span> | <span data-ttu-id="95f18-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="95f18-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95f18-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="95f18-112">Header</span></span><br/>  | <dl> <span data-ttu-id="95f18-113"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95f18-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95f18-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95f18-114">Library</span></span><br/> | <dl> <span data-ttu-id="95f18-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95f18-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f18-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95f18-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f18-117">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="95f18-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




