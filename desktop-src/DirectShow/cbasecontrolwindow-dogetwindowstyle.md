---
description: La méthode DoGetWindowStyle récupère les styles de fenêtre normaux ou étendus actuels.
ms.assetid: 1a854896-4bcb-49d0-92e4-40d1923712f9
title: Méthode CBaseControlWindow. DoGetWindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.DoGetWindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2667e4cbeef2d40bdc5bff8381ee3f07b3d0942f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533070"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="dbc51-103">Méthode CBaseControlWindow. DoGetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="dbc51-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="dbc51-104">La `DoGetWindowStyle` méthode récupère les styles de fenêtre standard actuels ou étendus.</span><span class="sxs-lookup"><span data-stu-id="dbc51-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbc51-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="dbc51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbc51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc51-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="dbc51-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="dbc51-108">Pointeur vers une variable qui reçoit les informations de style.</span><span class="sxs-lookup"><span data-stu-id="dbc51-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="dbc51-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="dbc51-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="dbc51-110">Valeur spécifiant les styles à récupérer.</span><span class="sxs-lookup"><span data-stu-id="dbc51-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="dbc51-111">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbc51-111">Must be one of the following:</span></span>



|              |                                      |
|--------------|--------------------------------------|
| <span data-ttu-id="dbc51-112">\_style GWL</span><span class="sxs-lookup"><span data-stu-id="dbc51-112">GWL\_STYLE</span></span>   | <span data-ttu-id="dbc51-113">Récupérer les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dbc51-113">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="dbc51-114">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="dbc51-114">GWL\_EXSTYLE</span></span> | <span data-ttu-id="dbc51-115">Récupérer les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="dbc51-115">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc51-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbc51-116">Return value</span></span>

<span data-ttu-id="dbc51-117">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbc51-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc51-118">Notes</span><span class="sxs-lookup"><span data-stu-id="dbc51-118">Remarks</span></span>

<span data-ttu-id="dbc51-119">Cette fonction membre appelle la fonction Win32 **GetWindowLong** pour récupérer le style de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dbc51-119">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="dbc51-120">Elle est appelée par les fonctions membres [**CBaseControlWindow :: obten \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) et [**CBaseControlWindow :: obten \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="dbc51-120">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc51-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbc51-121">Requirements</span></span>



| <span data-ttu-id="dbc51-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbc51-122">Requirement</span></span> | <span data-ttu-id="dbc51-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbc51-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc51-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dbc51-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc51-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc51-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dbc51-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dbc51-126">Library</span></span><br/> | <dl> <span data-ttu-id="dbc51-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc51-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc51-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbc51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc51-129">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="dbc51-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




