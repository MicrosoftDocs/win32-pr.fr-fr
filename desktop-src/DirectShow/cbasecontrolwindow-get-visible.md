---
description: La \_ méthode visible récupère la visibilité de la fenêtre active.
ms.assetid: 7e643569-1116-4562-be33-babd12a7e899
title: Méthode CBaseControlWindow.get_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc38a0b35f46de223ed84174c3b10f5300cc94d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537650"
---
# <a name="cbasecontrolwindowget_visible-method"></a><span data-ttu-id="760b7-103">CBaseControlWindow. obtient la \_ méthode visible</span><span class="sxs-lookup"><span data-stu-id="760b7-103">CBaseControlWindow.get\_Visible method</span></span>

<span data-ttu-id="760b7-104">La `get_Visible` méthode récupère la visibilité de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="760b7-104">The `get_Visible` method retrieves the current window visibility.</span></span>

## <a name="syntax"></a><span data-ttu-id="760b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="760b7-105">Syntax</span></span>


```C++
HRESULT get_Visible(
   long *pVisible
);
```



## <a name="parameters"></a><span data-ttu-id="760b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="760b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760b7-107">*pVisible*</span><span class="sxs-lookup"><span data-stu-id="760b7-107">*pVisible*</span></span> 
</dt> <dd>

<span data-ttu-id="760b7-108">Pointeur vers un indicateur booléen Automation (0 est désactivé, 1 est activé).</span><span class="sxs-lookup"><span data-stu-id="760b7-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760b7-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="760b7-109">Return value</span></span>

<span data-ttu-id="760b7-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="760b7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="760b7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="760b7-111">Remarks</span></span>

<span data-ttu-id="760b7-112">Cette fonction membre retourne 1 si la fenêtre a le \_ style WS visible ; sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="760b7-112">This member function returns  1 if the window has the WS\_VISIBLE style; 0 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="760b7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="760b7-113">Requirements</span></span>



| <span data-ttu-id="760b7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="760b7-114">Requirement</span></span> | <span data-ttu-id="760b7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="760b7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="760b7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="760b7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="760b7-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="760b7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="760b7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="760b7-118">Library</span></span><br/> | <dl> <span data-ttu-id="760b7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="760b7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="760b7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="760b7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760b7-121">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="760b7-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




