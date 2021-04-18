---
description: La \_ méthode obtenir FullScreenMode récupère le mode plein écran actuel.
ms.assetid: 351af361-5cfd-4e82-bd8a-92f629bd270d
title: Méthode CBaseControlWindow.get_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc77b43db2bb420e6cfe2eace44e96e1ab43b0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526756"
---
# <a name="cbasecontrolwindowget_fullscreenmode-method"></a><span data-ttu-id="f759d-103">Méthode CBaseControlWindow. obten \_ FullScreenMode</span><span class="sxs-lookup"><span data-stu-id="f759d-103">CBaseControlWindow.get\_FullScreenMode method</span></span>

<span data-ttu-id="f759d-104">La `get_FullScreenMode` méthode récupère le mode plein écran actuel.</span><span class="sxs-lookup"><span data-stu-id="f759d-104">The `get_FullScreenMode` method retrieves the current full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f759d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f759d-105">Syntax</span></span>


```C++
HRESULT get_FullScreenMode(
   long *FullScreenMode
);
```



## <a name="parameters"></a><span data-ttu-id="f759d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f759d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f759d-107">*FullScreenMode*</span><span class="sxs-lookup"><span data-stu-id="f759d-107">*FullScreenMode*</span></span> 
</dt> <dd>

<span data-ttu-id="f759d-108">Pointeur vers le mode plein écran actuel.</span><span class="sxs-lookup"><span data-stu-id="f759d-108">Pointer to the current full-screen mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f759d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f759d-109">Return value</span></span>

<span data-ttu-id="f759d-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f759d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f759d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f759d-111">Remarks</span></span>

<span data-ttu-id="f759d-112">Cette fonction membre retourne E \_ NOTIMPL par défaut.</span><span class="sxs-lookup"><span data-stu-id="f759d-112">This member function returns E\_NOTIMPL by default.</span></span> <span data-ttu-id="f759d-113">Cela informe le serveur de distribution de plug-in [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) que ce convertisseur n’implémente pas un convertisseur plein écran.</span><span class="sxs-lookup"><span data-stu-id="f759d-113">This informs the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) plug-in distributor that this renderer does not implement a full-screen renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f759d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f759d-114">Requirements</span></span>



| <span data-ttu-id="f759d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f759d-115">Requirement</span></span> | <span data-ttu-id="f759d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f759d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f759d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f759d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f759d-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f759d-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f759d-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f759d-119">Library</span></span><br/> | <dl> <span data-ttu-id="f759d-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f759d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f759d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f759d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f759d-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="f759d-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




