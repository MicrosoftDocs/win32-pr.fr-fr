---
description: La méthode SetPalette installe une palette pour la fenêtre. Cette méthode n’a aucun paramètre.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Méthode CBaseWindow. SetPalette (Winutil. h)-aucun paramètre
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104211978"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="d4c61-104">Méthode CBaseWindow. SetPalette (Winutil. h)-aucun paramètre</span><span class="sxs-lookup"><span data-stu-id="d4c61-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="d4c61-105">La `SetPalette` méthode installe une palette pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d4c61-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c61-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4c61-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="d4c61-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4c61-107">Parameters</span></span>

<span data-ttu-id="d4c61-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d4c61-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4c61-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4c61-109">Return value</span></span>

<span data-ttu-id="d4c61-110">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d4c61-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d4c61-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d4c61-111">Return code</span></span>                                                                             | <span data-ttu-id="d4c61-112">Description</span><span class="sxs-lookup"><span data-stu-id="d4c61-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="d4c61-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="d4c61-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="d4c61-114">Un appel interne à **GdiFlush** a retourné une erreur.</span><span class="sxs-lookup"><span data-stu-id="d4c61-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="d4c61-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4c61-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="d4c61-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d4c61-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d4c61-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d4c61-117">Remarks</span></span>

<span data-ttu-id="d4c61-118">La palette indiquée par la variable membre [**CBaseWindow :: m \_ HPALETTE**](cbasewindow-m-hpalette.md) est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="d4c61-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="d4c61-119">L’appelant doit garantir la validité de **m \_ HPALETTE**.</span><span class="sxs-lookup"><span data-stu-id="d4c61-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="d4c61-120">Si la valeur de la variable membre [**CBaseWindow :: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) est **false** (valeur par défaut), cette méthode sélectionne la palette et la réalise.</span><span class="sxs-lookup"><span data-stu-id="d4c61-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="d4c61-121">Dans le cas contraire, il sélectionne la palette, mais ne le réalise pas.</span><span class="sxs-lookup"><span data-stu-id="d4c61-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="d4c61-122">L’objet ne supprime pas les palettes précédentes qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="d4c61-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="d4c61-123">L’appelant est responsable de la suppression des palettes.</span><span class="sxs-lookup"><span data-stu-id="d4c61-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="d4c61-124">Tout thread peut appeler cette méthode en toute sécurité, pas seulement le thread qui possède la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d4c61-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="d4c61-125">La fenêtre envoie un message privé à lui-même, ce qui déclenche un appel à la méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d4c61-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c61-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4c61-126">Requirements</span></span>

| <span data-ttu-id="d4c61-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4c61-127">Requirement</span></span> | <span data-ttu-id="d4c61-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4c61-128">Value</span></span> |
|-|-|
| <span data-ttu-id="d4c61-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4c61-129">Header</span></span> | <span data-ttu-id="d4c61-130">Winutil. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="d4c61-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="d4c61-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4c61-131">Library</span></span>| <span data-ttu-id="d4c61-132">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="d4c61-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d4c61-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4c61-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c61-134">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="d4c61-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




