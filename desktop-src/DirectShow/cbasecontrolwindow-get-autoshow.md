---
description: La \_ méthode obtenir un affichage automatique récupère l’indicateur d’état d’affichage automatique actuel.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Méthode CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525380"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="329b0-103">CBaseControlWindow. obtient la \_ méthode d’affichage automatique</span><span class="sxs-lookup"><span data-stu-id="329b0-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="329b0-104">La `get_AutoShow` méthode récupère l’indicateur d’état d’affichage automatique actuel.</span><span class="sxs-lookup"><span data-stu-id="329b0-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="329b0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="329b0-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="329b0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="329b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329b0-107">*Affichage automatique*</span><span class="sxs-lookup"><span data-stu-id="329b0-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="329b0-108">Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).</span><span class="sxs-lookup"><span data-stu-id="329b0-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329b0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="329b0-109">Return value</span></span>

<span data-ttu-id="329b0-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="329b0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="329b0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="329b0-111">Remarks</span></span>

<span data-ttu-id="329b0-112">Cette fonction membre implémente la méthode d' [**\_ affichage automatique IVideoWindow :: obtient**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="329b0-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="329b0-113">Cette propriété simplifie l’accès à la fenêtre pour les applications.</span><span class="sxs-lookup"><span data-stu-id="329b0-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="329b0-114">Si cette valeur est définie sur 1 (activé), la fenêtre, qui est généralement masquée après la connexion du filtre, s’affiche automatiquement lorsque le filtre s’interrompt ou s’exécute.</span><span class="sxs-lookup"><span data-stu-id="329b0-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="329b0-115">Toutefois, la fenêtre ne doit pas être masquée quand le filtre s’arrête.</span><span class="sxs-lookup"><span data-stu-id="329b0-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="329b0-116">Si ce paramètre a la valeur 0 (OFF), la fenêtre est rendue visible uniquement lorsque l’application appelle [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_**](cbasecontrolwindow-put-windowstate.md) , avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="329b0-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="329b0-117">Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé.</span><span class="sxs-lookup"><span data-stu-id="329b0-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="329b0-118">Appelez la fonction membre [**CBaseControlWindow :: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="329b0-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="329b0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="329b0-119">Requirements</span></span>



| <span data-ttu-id="329b0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="329b0-120">Requirement</span></span> | <span data-ttu-id="329b0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="329b0-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329b0-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="329b0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="329b0-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="329b0-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="329b0-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="329b0-124">Library</span></span><br/> | <dl> <span data-ttu-id="329b0-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="329b0-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="329b0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="329b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329b0-127">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="329b0-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




