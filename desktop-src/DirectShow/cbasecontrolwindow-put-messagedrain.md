---
description: La \_ méthode put MessageDrain définit la fenêtre de façon à recevoir les messages de fenêtre envoyés au convertisseur vidéo.
ms.assetid: b2d2d489-a66f-474a-b8bf-b019179f6f69
title: Méthode CBaseControlWindow.put_MessageDrain (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f03f944a6af6ac99de6000a2507178eea510c06a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540642"
---
# <a name="cbasecontrolwindowput_messagedrain-method"></a><span data-ttu-id="1ec9d-103">CBaseControlWindow. put \_ MessageDrain, méthode</span><span class="sxs-lookup"><span data-stu-id="1ec9d-103">CBaseControlWindow.put\_MessageDrain method</span></span>

<span data-ttu-id="1ec9d-104">La `put_MessageDrain` méthode définit la fenêtre pour recevoir les messages de fenêtre envoyés au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-104">The `put_MessageDrain` method sets the window to receive window messages sent to the video renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ec9d-105">Syntax</span></span>


```C++
HRESULT put_MessageDrain(
   OAHWND Drain
);
```



## <a name="parameters"></a><span data-ttu-id="1ec9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ec9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec9d-107">*Vidage*</span><span class="sxs-lookup"><span data-stu-id="1ec9d-107">*Drain*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec9d-108">Fenêtre dans laquelle les messages doivent être publiés.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-108">Window to post messages to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec9d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ec9d-109">Return value</span></span>

<span data-ttu-id="1ec9d-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ec9d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec9d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1ec9d-111">Remarks</span></span>

<span data-ttu-id="1ec9d-112">Les messages envoyés au filtre de convertisseur vidéo peuvent être publiés dans une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-112">Messages sent to the video renderer filter can be posted to another window.</span></span> <span data-ttu-id="1ec9d-113">Cette fonction membre inscrit la fenêtre pour recevoir ces messages.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-113">This member function registers the window to receive these messages.</span></span> <span data-ttu-id="1ec9d-114">Contrairement à la fonction membre [**CBaseControlWindow ::p ut \_ owner**](cbasecontrolwindow-put-owner.md) , cette fonction membre ne rend pas la fenêtre vidéo enfant d’une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-114">Unlike the [**CBaseControlWindow::put\_Owner**](cbasecontrolwindow-put-owner.md) member function, this member function does not make the video window a child of another window.</span></span> <span data-ttu-id="1ec9d-115">Elle est particulièrement utile pour les convertisseurs vidéo en plein écran, qui ne peuvent pas être des fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="1ec9d-115">It is particularly useful for full-screen video renderers, which cannot be child windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec9d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ec9d-116">Requirements</span></span>



| <span data-ttu-id="1ec9d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ec9d-117">Requirement</span></span> | <span data-ttu-id="1ec9d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ec9d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec9d-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ec9d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec9d-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9d-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ec9d-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ec9d-121">Library</span></span><br/> | <dl> <span data-ttu-id="1ec9d-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec9d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec9d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ec9d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec9d-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="1ec9d-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




