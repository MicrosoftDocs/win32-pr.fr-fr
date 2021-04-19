---
description: La \_ méthode obtenir BorderColor récupère la couleur de bordure actuelle.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Méthode CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537385"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="af13b-103">CBaseControlWindow. obten, \_ méthode BorderColor</span><span class="sxs-lookup"><span data-stu-id="af13b-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="af13b-104">La `get_BorderColor` méthode récupère la couleur de bordure actuelle.</span><span class="sxs-lookup"><span data-stu-id="af13b-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="af13b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af13b-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="af13b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af13b-107">*Color*</span><span class="sxs-lookup"><span data-stu-id="af13b-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="af13b-108">Pointeur vers la couleur de bordure actuelle.</span><span class="sxs-lookup"><span data-stu-id="af13b-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af13b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af13b-109">Return value</span></span>

<span data-ttu-id="af13b-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af13b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af13b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="af13b-111">Remarks</span></span>

<span data-ttu-id="af13b-112">Une application peut définir un rectangle de destination dans lequel la vidéo doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="af13b-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="af13b-113">Ce rectangle est relatif à la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="af13b-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="af13b-114">Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une bordure entourant la vidéo.</span><span class="sxs-lookup"><span data-stu-id="af13b-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="af13b-115">Cette propriété affecte la couleur utilisée par la bordure.</span><span class="sxs-lookup"><span data-stu-id="af13b-115">This property affects the color used by the border.</span></span> <span data-ttu-id="af13b-116">Bien que le paramètre soit spécifié en tant que type **long** , il s’agit en fait d’une valeur **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="af13b-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="af13b-117">Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé.</span><span class="sxs-lookup"><span data-stu-id="af13b-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="af13b-118">Appelez la fonction membre [**CBaseControlWindow :: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="af13b-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="af13b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af13b-119">Requirements</span></span>



| <span data-ttu-id="af13b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af13b-120">Requirement</span></span> | <span data-ttu-id="af13b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="af13b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af13b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="af13b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="af13b-123"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af13b-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af13b-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af13b-124">Library</span></span><br/> | <dl> <span data-ttu-id="af13b-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af13b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af13b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af13b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af13b-127">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="af13b-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




