---
description: La méthode PrepareWindow crée la fenêtre.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Méthode CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540664"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="46e70-103">Méthode CBaseWindow. PrepareWindow</span><span class="sxs-lookup"><span data-stu-id="46e70-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="46e70-104">La `PrepareWindow` méthode crée la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="46e70-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46e70-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="46e70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46e70-106">Parameters</span></span>

<span data-ttu-id="46e70-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="46e70-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46e70-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46e70-108">Return value</span></span>

<span data-ttu-id="46e70-109">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46e70-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="46e70-110">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="46e70-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="46e70-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="46e70-111">Return code</span></span>                                                                            | <span data-ttu-id="46e70-112">Description</span><span class="sxs-lookup"><span data-stu-id="46e70-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="46e70-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46e70-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="46e70-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="46e70-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="46e70-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="46e70-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="46e70-116">Échec.</span><span class="sxs-lookup"><span data-stu-id="46e70-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46e70-117">Notes</span><span class="sxs-lookup"><span data-stu-id="46e70-117">Remarks</span></span>

<span data-ttu-id="46e70-118">Appelez cette méthode après avoir créé l’objet.</span><span class="sxs-lookup"><span data-stu-id="46e70-118">Call this method after creating the object.</span></span> <span data-ttu-id="46e70-119">Cette méthode effectue une comptabilité initiale, puis appelle la méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) pour créer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="46e70-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e70-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46e70-120">Requirements</span></span>



| <span data-ttu-id="46e70-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46e70-121">Requirement</span></span> | <span data-ttu-id="46e70-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="46e70-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e70-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="46e70-123">Header</span></span><br/>  | <dl> <span data-ttu-id="46e70-124"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46e70-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46e70-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46e70-125">Library</span></span><br/> | <dl> <span data-ttu-id="46e70-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46e70-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e70-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46e70-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e70-128">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="46e70-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




