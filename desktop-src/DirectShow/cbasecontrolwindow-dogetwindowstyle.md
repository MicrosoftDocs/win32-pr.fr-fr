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
ms.openlocfilehash: d970ee52203c5c8dfe8a897c5612604becc2b2e1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909817"
---
# <a name="cbasecontrolwindowdogetwindowstyle-method"></a><span data-ttu-id="e2a58-103">Méthode CBaseControlWindow. DoGetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="e2a58-103">CBaseControlWindow.DoGetWindowStyle method</span></span>

<span data-ttu-id="e2a58-104">La `DoGetWindowStyle` méthode récupère les styles de fenêtre standard actuels ou étendus.</span><span class="sxs-lookup"><span data-stu-id="e2a58-104">The `DoGetWindowStyle` method retrieves the current normal or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2a58-105">Syntax</span></span>


```C++
HRESULT DoGetWindowStyle(
   long *pStyle,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="e2a58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2a58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2a58-107">*pStyle*</span><span class="sxs-lookup"><span data-stu-id="e2a58-107">*pStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="e2a58-108">Pointeur vers une variable qui reçoit les informations de style.</span><span class="sxs-lookup"><span data-stu-id="e2a58-108">Pointer to a variable that receives the style information.</span></span>

</dd> <dt>

<span data-ttu-id="e2a58-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="e2a58-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="e2a58-110">Valeur spécifiant les styles à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e2a58-110">Value specifying which styles to retrieve.</span></span> <span data-ttu-id="e2a58-111">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e2a58-111">Must be one of the following:</span></span>



| <span data-ttu-id="e2a58-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="e2a58-112">Label</span></span> | <span data-ttu-id="e2a58-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2a58-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="e2a58-114">\_style GWL</span><span class="sxs-lookup"><span data-stu-id="e2a58-114">GWL\_STYLE</span></span>   | <span data-ttu-id="e2a58-115">Récupérer les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2a58-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="e2a58-116">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="e2a58-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="e2a58-117">Récupérer les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="e2a58-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2a58-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2a58-118">Return value</span></span>

<span data-ttu-id="e2a58-119">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e2a58-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2a58-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2a58-120">Remarks</span></span>

<span data-ttu-id="e2a58-121">Cette fonction membre appelle la fonction Win32 **GetWindowLong** pour récupérer le style de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e2a58-121">This member function calls the Win32 **GetWindowLong** function to retrieve the window style.</span></span> <span data-ttu-id="e2a58-122">Elle est appelée par les fonctions membres [**CBaseControlWindow :: obten \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md) et [**CBaseControlWindow :: obten \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="e2a58-122">It is called by the [**CBaseControlWindow::get\_WindowStyle**](cbasecontrolwindow-get-windowstyle.md) and [**CBaseControlWindow::get\_WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a58-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2a58-123">Requirements</span></span>



| <span data-ttu-id="e2a58-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2a58-124">Requirement</span></span> | <span data-ttu-id="e2a58-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2a58-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a58-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2a58-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e2a58-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2a58-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2a58-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2a58-128">Library</span></span><br/> | <dl> <span data-ttu-id="e2a58-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e2a58-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a58-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2a58-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a58-131">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="e2a58-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




