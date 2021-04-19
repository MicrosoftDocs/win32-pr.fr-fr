---
description: La méthode ActivateWindow dimensionne la fenêtre en fonction des exigences de la classe dérivée.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Méthode CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521640"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="17376-103">Méthode CBaseWindow. ActivateWindow</span><span class="sxs-lookup"><span data-stu-id="17376-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="17376-104">La `ActivateWindow` méthode dimensionne la fenêtre en fonction des spécifications de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="17376-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="17376-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17376-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="17376-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17376-106">Parameters</span></span>

<span data-ttu-id="17376-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="17376-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17376-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17376-108">Return value</span></span>

<span data-ttu-id="17376-109">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="17376-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="17376-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="17376-110">Return code</span></span>                                                                             | <span data-ttu-id="17376-111">Description</span><span class="sxs-lookup"><span data-stu-id="17376-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="17376-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="17376-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="17376-113">La fenêtre a déjà été activée.</span><span class="sxs-lookup"><span data-stu-id="17376-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="17376-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17376-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="17376-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="17376-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="17376-116">Notes</span><span class="sxs-lookup"><span data-stu-id="17376-116">Remarks</span></span>

<span data-ttu-id="17376-117">Cette méthode appelle la méthode [**CBaseWindow :: GetDefaultRect**](cbasewindow-getdefaultrect.md) pour déterminer la taille de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="17376-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="17376-118">La classe dérivée doit substituer **GetDefaultRect** pour retourner la taille des images qui seront affichées.</span><span class="sxs-lookup"><span data-stu-id="17376-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="17376-119">Si la fenêtre est déjà active, l’appel `ActivateWindow` de déplace la fenêtre vers le haut de l’ordre de plan, mais ne redimensionne pas la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="17376-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="17376-120">Il en va de même si la fenêtre a un parent.</span><span class="sxs-lookup"><span data-stu-id="17376-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="17376-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17376-121">Requirements</span></span>



| <span data-ttu-id="17376-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17376-122">Requirement</span></span> | <span data-ttu-id="17376-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="17376-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17376-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="17376-124">Header</span></span><br/>  | <dl> <span data-ttu-id="17376-125"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17376-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17376-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="17376-126">Library</span></span><br/> | <dl> <span data-ttu-id="17376-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="17376-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17376-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17376-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17376-129">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="17376-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




