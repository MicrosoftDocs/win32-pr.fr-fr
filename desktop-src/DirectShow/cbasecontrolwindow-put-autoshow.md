---
description: La \_ méthode placer un diaporama automatique définit l’indicateur d’état d’affichage automatique.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Méthode CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526054"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="1a60b-103">CBaseControlWindow. put, \_ méthode d’affichage automatique</span><span class="sxs-lookup"><span data-stu-id="1a60b-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="1a60b-104">La `put_AutoShow` méthode définit l’indicateur d’état d’affichage automatique.</span><span class="sxs-lookup"><span data-stu-id="1a60b-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a60b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a60b-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="1a60b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a60b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a60b-107">*Affichage automatique*</span><span class="sxs-lookup"><span data-stu-id="1a60b-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="1a60b-108">Indicateur booléen Automation (0 est désactivé, 1 est activé).</span><span class="sxs-lookup"><span data-stu-id="1a60b-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a60b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1a60b-109">Return value</span></span>

<span data-ttu-id="1a60b-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a60b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a60b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1a60b-111">Remarks</span></span>

<span data-ttu-id="1a60b-112">Cette propriété simplifie l’accès à la fenêtre pour les applications.</span><span class="sxs-lookup"><span data-stu-id="1a60b-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="1a60b-113">Si cette valeur est définie sur 1 (activé), la fenêtre, qui est généralement masquée après la connexion du filtre, s’affiche automatiquement lorsque le filtre s’interrompt ou s’exécute.</span><span class="sxs-lookup"><span data-stu-id="1a60b-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="1a60b-114">Toutefois, la fenêtre ne doit pas être masquée quand le filtre s’arrête.</span><span class="sxs-lookup"><span data-stu-id="1a60b-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="1a60b-115">Si la valeur est 0 (OFF), la fenêtre est visible uniquement quand l’application appelle [**CBaseControlWindow ::p ut \_ visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow ::p ut \_**](cbasecontrolwindow-put-windowstate.md) , avec les paramètres appropriés.</span><span class="sxs-lookup"><span data-stu-id="1a60b-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a60b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a60b-116">Requirements</span></span>



| <span data-ttu-id="1a60b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a60b-117">Requirement</span></span> | <span data-ttu-id="1a60b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a60b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a60b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1a60b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1a60b-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a60b-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a60b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1a60b-121">Library</span></span><br/> | <dl> <span data-ttu-id="1a60b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1a60b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a60b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a60b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a60b-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="1a60b-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




