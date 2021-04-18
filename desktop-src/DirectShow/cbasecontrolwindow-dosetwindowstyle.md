---
description: La méthode DoSetWindowStyle modifie les styles de fenêtre par défaut ou étendus.
ms.assetid: 4a9a97fb-b527-44ce-af8c-e5ea832ed4c4
title: Méthode CBaseControlWindow. DoSetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoSetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d57d023dff803caf5da7e61dea266670ec8bde5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540353"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="346e5-103">Méthode CBaseControlWindow. DoSetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="346e5-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="346e5-104">La `DoSetWindowStyle` méthode modifie les styles de fenêtre par défaut ou étendus.</span><span class="sxs-lookup"><span data-stu-id="346e5-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="346e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="346e5-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="346e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="346e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="346e5-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="346e5-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="346e5-108">Styles de fenêtre appropriés.</span><span class="sxs-lookup"><span data-stu-id="346e5-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="346e5-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="346e5-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="346e5-110">Valeur spécifiant les styles à définir.</span><span class="sxs-lookup"><span data-stu-id="346e5-110">Value specifying which styles to set.</span></span> <span data-ttu-id="346e5-111">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="346e5-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="346e5-112">\_style GWL</span><span class="sxs-lookup"><span data-stu-id="346e5-112">GWL\_STYLE</span></span>   | <span data-ttu-id="346e5-113">Récupérer les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="346e5-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="346e5-114">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="346e5-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="346e5-115">Récupérer les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="346e5-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="346e5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="346e5-116">Return value</span></span>

<span data-ttu-id="346e5-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="346e5-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="346e5-118">Notes</span><span class="sxs-lookup"><span data-stu-id="346e5-118">Remarks</span></span>

<span data-ttu-id="346e5-119">Cette fonction membre appelle la fonction Win32 **SetWindowLong** pour définir le style de la fenêtre, puis réaffiche la fenêtre dans la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="346e5-119">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="346e5-120">Cette fonction membre est appelée par les fonctions membres [**CBaseControlWindow ::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) et [**CBaseControlWindow ::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="346e5-120">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="346e5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="346e5-121">Requirements</span></span>



| <span data-ttu-id="346e5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="346e5-122">Requirement</span></span> | <span data-ttu-id="346e5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="346e5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="346e5-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="346e5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="346e5-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="346e5-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="346e5-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="346e5-126">Library</span></span><br/> | <dl> <span data-ttu-id="346e5-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="346e5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="346e5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="346e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="346e5-129">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="346e5-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




