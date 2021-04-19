---
description: La méthode DoCreateWindow crée la fenêtre.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCméthode reateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535878"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="9ebb8-103">CBaseWindow.DoCméthode reateWindow</span><span class="sxs-lookup"><span data-stu-id="9ebb8-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="9ebb8-104">La `DoCreateWindow` méthode crée la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9ebb8-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ebb8-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="9ebb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ebb8-106">Parameters</span></span>

<span data-ttu-id="9ebb8-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9ebb8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ebb8-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ebb8-108">Return value</span></span>

<span data-ttu-id="9ebb8-109">Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.</span><span class="sxs-lookup"><span data-stu-id="9ebb8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebb8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9ebb8-110">Remarks</span></span>

<span data-ttu-id="9ebb8-111">La méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9ebb8-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebb8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ebb8-112">Requirements</span></span>



| <span data-ttu-id="9ebb8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ebb8-113">Requirement</span></span> | <span data-ttu-id="9ebb8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ebb8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebb8-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ebb8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9ebb8-116"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ebb8-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9ebb8-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ebb8-117">Library</span></span><br/> | <dl> <span data-ttu-id="9ebb8-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9ebb8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ebb8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ebb8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebb8-120">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="9ebb8-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




