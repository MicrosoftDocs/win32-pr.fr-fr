---
description: Méthode constructeur CBaseWindow. CBaseWindow.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructeur CBaseWindow. CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095817"
---
# <a name="cbasewindowcbasewindow-constructor"></a><span data-ttu-id="41254-103">Constructeur CBaseWindow. CBaseWindow</span><span class="sxs-lookup"><span data-stu-id="41254-103">CBaseWindow.CBaseWindow constructor</span></span>

<span data-ttu-id="41254-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="41254-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="41254-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41254-105">Syntax</span></span>


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="41254-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41254-107">*bDoGetDC*</span><span class="sxs-lookup"><span data-stu-id="41254-107">*bDoGetDC*</span></span> 
</dt> <dd>

<span data-ttu-id="41254-108">Valeur booléenne qui spécifie s’il faut récupérer le contexte de périphérique (Device Context).</span><span class="sxs-lookup"><span data-stu-id="41254-108">Boolean value that specifies whether to retrieve the device context.</span></span>

</dd> <dt>

<span data-ttu-id="41254-109">*bPostToDestroy*</span><span class="sxs-lookup"><span data-stu-id="41254-109">*bPostToDestroy*</span></span> 
</dt> <dd>

<span data-ttu-id="41254-110">Valeur booléenne qui spécifie la variable membre [**CBaseWindow :: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .</span><span class="sxs-lookup"><span data-stu-id="41254-110">Boolean value that specifies the [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) member variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41254-111">Notes </span><span class="sxs-lookup"><span data-stu-id="41254-111">Remarks</span></span>

<span data-ttu-id="41254-112">Après avoir créé l’objet, appelez la méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) pour créer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41254-112">After you create the object, call the [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method to create the window.</span></span> <span data-ttu-id="41254-113">**PrepareWindow** est une méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="41254-113">**PrepareWindow** is a virtual method.</span></span> <span data-ttu-id="41254-114">Elle appelle [**CBaseWindow :: InitialiseWindow**](cbasewindow-initialisewindow.md), également une méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="41254-114">It calls [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md), also a virtual method.</span></span> <span data-ttu-id="41254-115">Ces méthodes sont séparées du constructeur afin que les classes dérivées puissent les remplacer, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="41254-115">These methods are separated from the constructor so that derived classes can override them, if necessary.</span></span>

<span data-ttu-id="41254-116">Si la valeur du paramètre *bDoGetDC* est **true**, l' `CBaseWindow` objet récupère un handle vers le contexte de périphérique (DC) de la fenêtre et le stocke dans la variable membre [**CBaseWindow :: m \_ HDC**](cbasewindow-m-hdc.md) .</span><span class="sxs-lookup"><span data-stu-id="41254-116">If the value of the *bDoGetDC* parameter is **TRUE**, the `CBaseWindow` object retrieves a handle to the window's device context (DC) and stores it in the [**CBaseWindow::m\_hdc**](cbasewindow-m-hdc.md) member variable.</span></span> <span data-ttu-id="41254-117">L’objet crée également un contrôleur de stockage de mémoire compatible, qu’il stocke dans la variable membre [**CBaseWindow :: m \_ MemoryDC**](cbasewindow-m-memorydc.md) .</span><span class="sxs-lookup"><span data-stu-id="41254-117">The object also creates a compatible memory DC, which it stores in the [**CBaseWindow::m\_MemoryDC**](cbasewindow-m-memorydc.md) member variable.</span></span> <span data-ttu-id="41254-118">Ces actions se produisent dans la méthode **InitialiseWindow** .</span><span class="sxs-lookup"><span data-stu-id="41254-118">These actions occur in the **InitialiseWindow** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="41254-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41254-119">Requirements</span></span>



| <span data-ttu-id="41254-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41254-120">Requirement</span></span> | <span data-ttu-id="41254-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="41254-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41254-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="41254-122">Header</span></span><br/>  | <dl> <span data-ttu-id="41254-123"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41254-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="41254-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="41254-124">Library</span></span><br/> | <dl> <span data-ttu-id="41254-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="41254-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41254-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41254-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41254-127">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="41254-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




