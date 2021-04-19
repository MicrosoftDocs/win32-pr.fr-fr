---
description: La méthode OnPaletteChange gère les messages de modification de palette.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Méthode CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538086"
---
# <a name="cbasewindowonpalettechange-method"></a><span data-ttu-id="cdee4-103">Méthode CBaseWindow. OnPaletteChange</span><span class="sxs-lookup"><span data-stu-id="cdee4-103">CBaseWindow.OnPaletteChange method</span></span>

<span data-ttu-id="cdee4-104">La `OnPaletteChange` méthode gère les messages de modification de palette.</span><span class="sxs-lookup"><span data-stu-id="cdee4-104">The `OnPaletteChange` method handles palette-change messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdee4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdee4-105">Syntax</span></span>


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a><span data-ttu-id="cdee4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdee4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdee4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="cdee4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cdee4-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cdee4-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="cdee4-109">*Message*</span><span class="sxs-lookup"><span data-stu-id="cdee4-109">*Message*</span></span> 
</dt> <dd>

<span data-ttu-id="cdee4-110">Identificateur du message.</span><span class="sxs-lookup"><span data-stu-id="cdee4-110">Message identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdee4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdee4-111">Return value</span></span>

<span data-ttu-id="cdee4-112">Retourne 0 si le message a été traité, ou 1 si le message n’a pas été traité.</span><span class="sxs-lookup"><span data-stu-id="cdee4-112">Returns 0 if the message was processed, or 1 if the message was not processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdee4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cdee4-113">Remarks</span></span>

<span data-ttu-id="cdee4-114">Cette méthode gère \_ les messages WM PALETTECHANGED et WM \_ QUERYNEWPALETTE.</span><span class="sxs-lookup"><span data-stu-id="cdee4-114">This method handles WM\_PALETTECHANGED and WM\_QUERYNEWPALETTE messages.</span></span> <span data-ttu-id="cdee4-115">Elle appelle la méthode [**CBaseWindow ::D orealisepalette**](cbasewindow-dorealisepalette.md) pour réaliser la nouvelle palette.</span><span class="sxs-lookup"><span data-stu-id="cdee4-115">It calls the [**CBaseWindow::DoRealisePalette**](cbasewindow-dorealisepalette.md) method to realize the new palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdee4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdee4-116">Requirements</span></span>



| <span data-ttu-id="cdee4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdee4-117">Requirement</span></span> | <span data-ttu-id="cdee4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdee4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdee4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdee4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cdee4-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdee4-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cdee4-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cdee4-121">Library</span></span><br/> | <dl> <span data-ttu-id="cdee4-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cdee4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdee4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdee4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdee4-124">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="cdee4-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




