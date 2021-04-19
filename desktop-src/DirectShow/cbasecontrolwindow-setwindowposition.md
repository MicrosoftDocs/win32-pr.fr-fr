---
description: La méthode SetWindowPosition définit la position de la fenêtre sur le bureau.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Méthode CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541348"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a><span data-ttu-id="95612-103">Méthode CBaseControlWindow. SetWindowPosition</span><span class="sxs-lookup"><span data-stu-id="95612-103">CBaseControlWindow.SetWindowPosition method</span></span>

<span data-ttu-id="95612-104">La `SetWindowPosition` méthode définit la position de la fenêtre sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="95612-104">The `SetWindowPosition` method sets the window position on the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="95612-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95612-105">Syntax</span></span>


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="95612-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95612-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="95612-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="95612-108">Nouvelle coordonnée gauche.</span><span class="sxs-lookup"><span data-stu-id="95612-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="95612-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="95612-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="95612-110">Nouvelle coordonnée supérieure.</span><span class="sxs-lookup"><span data-stu-id="95612-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="95612-111">*Width*</span><span class="sxs-lookup"><span data-stu-id="95612-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="95612-112">Largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="95612-112">Width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="95612-113">*Height*</span><span class="sxs-lookup"><span data-stu-id="95612-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="95612-114">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="95612-114">Height of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95612-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95612-115">Return value</span></span>

<span data-ttu-id="95612-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95612-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95612-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95612-117">Requirements</span></span>



| <span data-ttu-id="95612-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95612-118">Requirement</span></span> | <span data-ttu-id="95612-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="95612-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95612-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="95612-120">Header</span></span><br/>  | <dl> <span data-ttu-id="95612-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95612-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="95612-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95612-122">Library</span></span><br/> | <dl> <span data-ttu-id="95612-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95612-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95612-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95612-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95612-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="95612-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




