---
description: La méthode SetPalette installe une palette pour la fenêtre.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Méthode CBaseWindow. SetPalette (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543789"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="7a8aa-103">Méthode CBaseWindow. SetPalette (Winutil. h)</span><span class="sxs-lookup"><span data-stu-id="7a8aa-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="7a8aa-104">La `SetPalette` méthode installe une palette pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a8aa-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="7a8aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a8aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a8aa-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="7a8aa-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="7a8aa-108">Handle vers la nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-108">Handle to the new palette.</span></span> <span data-ttu-id="7a8aa-109">Ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a8aa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a8aa-110">Return value</span></span>

<span data-ttu-id="7a8aa-111">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7a8aa-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7a8aa-112">Return code</span></span>                                                                             | <span data-ttu-id="7a8aa-113">Description</span><span class="sxs-lookup"><span data-stu-id="7a8aa-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="7a8aa-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7a8aa-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7a8aa-115">Un appel interne à **GdiFlush** a retourné une erreur.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="7a8aa-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a8aa-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7a8aa-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="7a8aa-118">Notes</span><span class="sxs-lookup"><span data-stu-id="7a8aa-118">Remarks</span></span>

<span data-ttu-id="7a8aa-119">Si la valeur de la variable membre [**CBaseWindow :: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) est **false** (valeur par défaut), cette méthode sélectionne la palette et la réalise.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="7a8aa-120">Dans le cas contraire, il sélectionne la palette, mais ne le réalise pas.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="7a8aa-121">L’objet ne supprime pas les palettes précédentes qu’il utilisait.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="7a8aa-122">L’appelant est responsable de la suppression des palettes.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="7a8aa-123">Tout thread peut appeler cette méthode en toute sécurité, pas seulement le thread qui possède la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="7a8aa-124">La fenêtre envoie un message privé à lui-même, ce qui déclenche un appel à la méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) .</span><span class="sxs-lookup"><span data-stu-id="7a8aa-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a8aa-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a8aa-125">Requirements</span></span>



| <span data-ttu-id="7a8aa-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a8aa-126">Requirement</span></span> | <span data-ttu-id="7a8aa-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a8aa-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8aa-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a8aa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7a8aa-129"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a8aa-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a8aa-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7a8aa-130">Library</span></span><br/> | <dl> <span data-ttu-id="7a8aa-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a8aa-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a8aa-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a8aa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a8aa-133">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="7a8aa-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




