---
description: La méthode SetWindowForeground déplace la fenêtre vidéo au premier plan et, éventuellement, lui donne le focus.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Méthode CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533247"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="152d4-103">Méthode CBaseControlWindow. SetWindowForeground</span><span class="sxs-lookup"><span data-stu-id="152d4-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="152d4-104">La `SetWindowForeground` méthode déplace la fenêtre vidéo au premier plan et, éventuellement, lui donne le focus.</span><span class="sxs-lookup"><span data-stu-id="152d4-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="152d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="152d4-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="152d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="152d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152d4-107">*Priorité*</span><span class="sxs-lookup"><span data-stu-id="152d4-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="152d4-108">Valeur qui spécifie si la fenêtre vidéo obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="152d4-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="152d4-109">La valeur 1 donne le focus de la fenêtre et 0 ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="152d4-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152d4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="152d4-110">Return value</span></span>

<span data-ttu-id="152d4-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="152d4-111">Returns one of the following values.</span></span>



| <span data-ttu-id="152d4-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="152d4-112">Return code</span></span>                                                                                           | <span data-ttu-id="152d4-113">Description</span><span class="sxs-lookup"><span data-stu-id="152d4-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="152d4-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="152d4-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="152d4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="152d4-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="152d4-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="152d4-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="152d4-117">Le focus n’est pas égal à 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="152d4-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="152d4-118"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="152d4-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="152d4-119">Le filtre actuel n’est pas connecté à un graphique de filtre complet.</span><span class="sxs-lookup"><span data-stu-id="152d4-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="152d4-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="152d4-120">Requirements</span></span>



| <span data-ttu-id="152d4-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="152d4-121">Requirement</span></span> | <span data-ttu-id="152d4-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="152d4-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="152d4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="152d4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="152d4-124"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="152d4-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="152d4-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="152d4-125">Library</span></span><br/> | <dl> <span data-ttu-id="152d4-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="152d4-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152d4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152d4-128">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="152d4-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




