---
description: La méthode DoSetWindowForeground amène la fenêtre au premier plan.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Méthode CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532537"
---
# <a name="cbasewindowdosetwindowforeground-method"></a><span data-ttu-id="89632-103">Méthode CBaseWindow. DoSetWindowForeground</span><span class="sxs-lookup"><span data-stu-id="89632-103">CBaseWindow.DoSetWindowForeground method</span></span>

<span data-ttu-id="89632-104">La `DoSetWindowForeground` méthode amène la fenêtre au premier plan.</span><span class="sxs-lookup"><span data-stu-id="89632-104">The `DoSetWindowForeground` method brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="89632-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89632-105">Syntax</span></span>


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a><span data-ttu-id="89632-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89632-107">*bFocus*</span><span class="sxs-lookup"><span data-stu-id="89632-107">*bFocus*</span></span> 
</dt> <dd>

<span data-ttu-id="89632-108">Valeur booléenne qui spécifie s’il faut attribuer le focus à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="89632-108">Boolean value that specifies whether to give the window focus.</span></span> <span data-ttu-id="89632-109">Si la valeur est **true**, la fenêtre obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="89632-109">If the value is **TRUE**, the window gains focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89632-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89632-110">Return value</span></span>

<span data-ttu-id="89632-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="89632-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89632-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89632-112">Requirements</span></span>



| <span data-ttu-id="89632-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89632-113">Requirement</span></span> | <span data-ttu-id="89632-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="89632-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89632-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="89632-115">Header</span></span><br/>  | <dl> <span data-ttu-id="89632-116"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89632-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89632-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="89632-117">Library</span></span><br/> | <dl> <span data-ttu-id="89632-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89632-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89632-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89632-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89632-120">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="89632-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




