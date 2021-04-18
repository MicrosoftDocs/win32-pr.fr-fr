---
description: La \_ méthode put BorderColor modifie la couleur de la bordure.
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: Méthode CBaseControlWindow.put_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533078"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a><span data-ttu-id="fcfc0-103">CBaseControlWindow. put \_ BorderColor, méthode</span><span class="sxs-lookup"><span data-stu-id="fcfc0-103">CBaseControlWindow.put\_BorderColor method</span></span>

<span data-ttu-id="fcfc0-104">La `put_BorderColor` méthode modifie la couleur de la bordure.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-104">The `put_BorderColor` method changes the border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcfc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fcfc0-105">Syntax</span></span>


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a><span data-ttu-id="fcfc0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fcfc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcfc0-107">*Color*</span><span class="sxs-lookup"><span data-stu-id="fcfc0-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="fcfc0-108">Nouvelle couleur de bordure.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-108">New border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcfc0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fcfc0-109">Return value</span></span>

<span data-ttu-id="fcfc0-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fcfc0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcfc0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fcfc0-111">Remarks</span></span>

<span data-ttu-id="fcfc0-112">Une application peut établir un rectangle de destination dans lequel la vidéo doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-112">An application can establish a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="fcfc0-113">Ce rectangle est relatif à la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="fcfc0-114">Si cette opération est effectuée (la valeur par défaut consiste à toujours peindre la totalité de la fenêtre), il y a une bordure entourant la vidéo.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="fcfc0-115">Cette propriété affecte la couleur utilisée par la bordure.</span><span class="sxs-lookup"><span data-stu-id="fcfc0-115">This property affects the color used by the border.</span></span> <span data-ttu-id="fcfc0-116">Bien que le paramètre soit spécifié en tant que type **long** , il s’agit en fait d’une valeur **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="fcfc0-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfc0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fcfc0-117">Requirements</span></span>



| <span data-ttu-id="fcfc0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fcfc0-118">Requirement</span></span> | <span data-ttu-id="fcfc0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fcfc0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfc0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fcfc0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fcfc0-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfc0-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fcfc0-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fcfc0-122">Library</span></span><br/> | <dl> <span data-ttu-id="fcfc0-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfc0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcfc0-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcfc0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfc0-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="fcfc0-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




