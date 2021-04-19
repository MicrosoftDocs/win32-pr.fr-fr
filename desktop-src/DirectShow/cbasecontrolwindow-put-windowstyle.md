---
description: La \_ méthode put WindowStyle définit les styles de fenêtre standard.
ms.assetid: 3b3aa035-6aa1-4f11-80d8-03268fcf98e1
title: Méthode CBaseControlWindow.put_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f98e6205a45530a0dbcce09d095dfaa2267ccbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541531"
---
# <a name="cbasecontrolwindowput_windowstyle-method"></a><span data-ttu-id="8d84b-103">CBaseControlWindow. put, \_ méthode WindowStyle</span><span class="sxs-lookup"><span data-stu-id="8d84b-103">CBaseControlWindow.put\_WindowStyle method</span></span>

<span data-ttu-id="8d84b-104">La `put_WindowStyle` méthode définit les styles de fenêtre standard.</span><span class="sxs-lookup"><span data-stu-id="8d84b-104">The `put_WindowStyle` method sets the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d84b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d84b-105">Syntax</span></span>


```C++
HRESULT put_WindowStyle(
   long WindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="8d84b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d84b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d84b-107">*WindowStyle*</span><span class="sxs-lookup"><span data-stu-id="8d84b-107">*WindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="8d84b-108">Nouveaux styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8d84b-108">New window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d84b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d84b-109">Return value</span></span>

<span data-ttu-id="8d84b-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8d84b-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d84b-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d84b-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d84b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8d84b-112">Remarks</span></span>

<span data-ttu-id="8d84b-113">Soyez vigilant lorsque vous modifiez les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8d84b-113">Take care when changing the window styles.</span></span> <span data-ttu-id="8d84b-114">Dans la plupart des cas, une application doit récupérer le style actuel, puis ajouter ou supprimer les bits inappropriés.</span><span class="sxs-lookup"><span data-stu-id="8d84b-114">In most cases, an application should retrieve the current style and then add or remove the inappropriate bits.</span></span> <span data-ttu-id="8d84b-115">Cette procédure permet à différents styles de fenêtre internes utilisés par Windows de rester intacts.</span><span class="sxs-lookup"><span data-stu-id="8d84b-115">This procedure allows various internal window styles used by Windows to remain intact.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d84b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d84b-116">Requirements</span></span>



| <span data-ttu-id="8d84b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d84b-117">Requirement</span></span> | <span data-ttu-id="8d84b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d84b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d84b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d84b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8d84b-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d84b-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d84b-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d84b-121">Library</span></span><br/> | <dl> <span data-ttu-id="8d84b-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d84b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d84b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d84b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d84b-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="8d84b-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




