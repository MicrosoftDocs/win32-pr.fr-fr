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
ms.openlocfilehash: db88c5818d31d65f361ae1a805bd50c285d4a5c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909807"
---
# <a name="cbasecontrolwindowdosetwindowstyle-method"></a><span data-ttu-id="37763-103">Méthode CBaseControlWindow. DoSetWindowStyle</span><span class="sxs-lookup"><span data-stu-id="37763-103">CBaseControlWindow.DoSetWindowStyle method</span></span>

<span data-ttu-id="37763-104">La `DoSetWindowStyle` méthode modifie les styles de fenêtre par défaut ou étendus.</span><span class="sxs-lookup"><span data-stu-id="37763-104">The `DoSetWindowStyle` method changes the typical or extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="37763-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37763-105">Syntax</span></span>


```C++
HRESULT DoSetWindowStyle(
   long Style,
   long WindowLong
);
```



## <a name="parameters"></a><span data-ttu-id="37763-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37763-107">*Style*</span><span class="sxs-lookup"><span data-stu-id="37763-107">*Style*</span></span> 
</dt> <dd>

<span data-ttu-id="37763-108">Styles de fenêtre appropriés.</span><span class="sxs-lookup"><span data-stu-id="37763-108">Appropriate window styles.</span></span>

</dd> <dt>

<span data-ttu-id="37763-109">*WindowLong*</span><span class="sxs-lookup"><span data-stu-id="37763-109">*WindowLong*</span></span> 
</dt> <dd>

<span data-ttu-id="37763-110">Valeur spécifiant les styles à définir.</span><span class="sxs-lookup"><span data-stu-id="37763-110">Value specifying which styles to set.</span></span> <span data-ttu-id="37763-111">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="37763-111">Must be one of the following:</span></span>



| <span data-ttu-id="37763-112">Étiquette</span><span class="sxs-lookup"><span data-stu-id="37763-112">Label</span></span> | <span data-ttu-id="37763-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="37763-113">Value</span></span> |
|--------------|--------------------------------------|
| <span data-ttu-id="37763-114">\_style GWL</span><span class="sxs-lookup"><span data-stu-id="37763-114">GWL\_STYLE</span></span>   | <span data-ttu-id="37763-115">Récupérer les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="37763-115">Retrieve the window styles.</span></span>          |
| <span data-ttu-id="37763-116">GWL \_ EXstyle</span><span class="sxs-lookup"><span data-stu-id="37763-116">GWL\_EXSTYLE</span></span> | <span data-ttu-id="37763-117">Récupérer les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="37763-117">Retrieve the extended window styles.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37763-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="37763-118">Return value</span></span>

<span data-ttu-id="37763-119">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="37763-119">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37763-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="37763-120">Remarks</span></span>

<span data-ttu-id="37763-121">Cette fonction membre appelle la fonction Win32 **SetWindowLong** pour définir le style de la fenêtre, puis réaffiche la fenêtre dans la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="37763-121">This member function calls the Win32 **SetWindowLong** function to set the window style, and then redisplays the window in the current position.</span></span> <span data-ttu-id="37763-122">Cette fonction membre est appelée par les fonctions membres [**CBaseControlWindow ::p ut \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md) et [**CBaseControlWindow ::p ut \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) .</span><span class="sxs-lookup"><span data-stu-id="37763-122">This member function is called by the [**CBaseControlWindow::put\_WindowStyle**](cbasecontrolwindow-put-windowstyle.md) and [**CBaseControlWindow::put\_WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md) member functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="37763-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37763-123">Requirements</span></span>



| <span data-ttu-id="37763-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37763-124">Requirement</span></span> | <span data-ttu-id="37763-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="37763-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37763-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="37763-126">Header</span></span><br/>  | <dl> <span data-ttu-id="37763-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37763-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37763-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37763-128">Library</span></span><br/> | <dl> <span data-ttu-id="37763-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="37763-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37763-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37763-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37763-131">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="37763-131">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




