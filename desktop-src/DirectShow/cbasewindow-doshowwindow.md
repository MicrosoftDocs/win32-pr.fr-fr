---
description: La méthode DoShowWindow définit l’état d’affichage de la fenêtre.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Méthode CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544090"
---
# <a name="cbasewindowdoshowwindow-method"></a><span data-ttu-id="ec3b7-103">Méthode CBaseWindow. DoShowWindow</span><span class="sxs-lookup"><span data-stu-id="ec3b7-103">CBaseWindow.DoShowWindow method</span></span>

<span data-ttu-id="ec3b7-104">La méthode **DoShowWindow** définit l’état d’affichage de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ec3b7-104">The **DoShowWindow** method sets the window's show state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec3b7-105">Syntax</span></span>


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a><span data-ttu-id="ec3b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec3b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3b7-107">*ShowCmd*</span><span class="sxs-lookup"><span data-stu-id="ec3b7-107">*ShowCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="ec3b7-108">Indicateur qui spécifie la façon dont la fenêtre doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="ec3b7-108">Flag that specifies how the window is to be shown.</span></span> <span data-ttu-id="ec3b7-109">La valeur peut être toute constante définie pour le paramètre *nCmdShow* de la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="ec3b7-109">The value can be any constant defined for the *nCmdShow* parameter of the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3b7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec3b7-110">Return value</span></span>

<span data-ttu-id="ec3b7-111">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ec3b7-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec3b7-112">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec3b7-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3b7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec3b7-113">Requirements</span></span>



| <span data-ttu-id="ec3b7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec3b7-114">Requirement</span></span> | <span data-ttu-id="ec3b7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec3b7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3b7-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec3b7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ec3b7-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3b7-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ec3b7-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec3b7-118">Library</span></span><br/> | <dl> <span data-ttu-id="ec3b7-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec3b7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3b7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec3b7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3b7-121">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="ec3b7-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

