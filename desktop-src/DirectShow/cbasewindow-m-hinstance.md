---
description: Handle de l’instance de module.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membre CBaseWindow :: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532549"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="3a63f-103">CBaseWindow :: m \_ membre HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="3a63f-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="3a63f-104">Handle de l’instance de module.</span><span class="sxs-lookup"><span data-stu-id="3a63f-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a63f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a63f-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="3a63f-106">Notes</span><span class="sxs-lookup"><span data-stu-id="3a63f-106">Remarks</span></span>

<span data-ttu-id="3a63f-107">La fonction de point d’entrée DLL définit une variable globale avec un handle vers l’instance de module.</span><span class="sxs-lookup"><span data-stu-id="3a63f-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="3a63f-108">La classe **CBaseWindow** stocke ce handle dans sa méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3a63f-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a63f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a63f-109">Requirements</span></span>



| <span data-ttu-id="3a63f-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a63f-110">Requirement</span></span> | <span data-ttu-id="3a63f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a63f-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a63f-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a63f-112">Header</span></span><br/>  | <dl> <span data-ttu-id="3a63f-113"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a63f-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a63f-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a63f-114">Library</span></span><br/> | <dl> <span data-ttu-id="3a63f-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a63f-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a63f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a63f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a63f-117">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="3a63f-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




