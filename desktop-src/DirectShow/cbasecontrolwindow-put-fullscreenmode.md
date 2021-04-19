---
description: La \_ méthode put FullScreenMode définit le mode plein écran du convertisseur.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Méthode CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524026"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a><span data-ttu-id="87f10-103">CBaseControlWindow. put \_ FullScreenMode, méthode</span><span class="sxs-lookup"><span data-stu-id="87f10-103">CBaseControlWindow.put\_FullScreenMode method</span></span>

<span data-ttu-id="87f10-104">La `put_FullScreenMode` méthode définit le mode plein écran du convertisseur.</span><span class="sxs-lookup"><span data-stu-id="87f10-104">The `put_FullScreenMode` method sets the full-screen mode of the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87f10-105">Syntax</span></span>


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="87f10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87f10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87f10-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="87f10-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="87f10-108">Mode plein écran à appliquer.</span><span class="sxs-lookup"><span data-stu-id="87f10-108">Full-screen mode to apply.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87f10-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87f10-109">Return value</span></span>

<span data-ttu-id="87f10-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87f10-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87f10-111">L’implémentation actuelle retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="87f10-111">The current implementation returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f10-112">Notes</span><span class="sxs-lookup"><span data-stu-id="87f10-112">Remarks</span></span>

<span data-ttu-id="87f10-113">Un convertisseur vidéo qui implémente un mode plein écran doit substituer cette fonction membre et implémenter les modes pris en charge.</span><span class="sxs-lookup"><span data-stu-id="87f10-113">A video renderer that implements a full-screen mode should override this member function and implement whatever modes it supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f10-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87f10-114">Requirements</span></span>



| <span data-ttu-id="87f10-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87f10-115">Requirement</span></span> | <span data-ttu-id="87f10-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="87f10-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f10-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="87f10-117">Header</span></span><br/>  | <dl> <span data-ttu-id="87f10-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87f10-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87f10-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87f10-119">Library</span></span><br/> | <dl> <span data-ttu-id="87f10-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87f10-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f10-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87f10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f10-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="87f10-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




