---
description: La \_ méthode put Caption définit le titre ou la légende de la fenêtre.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Méthode CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538772"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="8a41c-103">CBaseControlWindow. put, \_ méthode de légende</span><span class="sxs-lookup"><span data-stu-id="8a41c-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="8a41c-104">La `put_Caption` méthode définit le titre ou la légende de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8a41c-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a41c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a41c-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="8a41c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a41c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a41c-107">*strCaption*</span><span class="sxs-lookup"><span data-stu-id="8a41c-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="8a41c-108">Nouvelle légende de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8a41c-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a41c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a41c-109">Return value</span></span>

<span data-ttu-id="8a41c-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a41c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a41c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8a41c-111">Remarks</span></span>

<span data-ttu-id="8a41c-112">La plupart des fenêtres de niveau supérieur sur un bureau Windows ont un titre (légende) qui leur est associé.</span><span class="sxs-lookup"><span data-stu-id="8a41c-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="8a41c-113">Cette propriété peut être interrogée et définie par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="8a41c-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="8a41c-114">Tout jeu de légendes est visible uniquement si le style de légende WS est appliqué à la fenêtre \_ .</span><span class="sxs-lookup"><span data-stu-id="8a41c-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="8a41c-115">Si ce n’est pas le cas, la légende peut toujours être définie (et Récupérée), bien qu’elle ne soit pas visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8a41c-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a41c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a41c-116">Requirements</span></span>



| <span data-ttu-id="8a41c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a41c-117">Requirement</span></span> | <span data-ttu-id="8a41c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a41c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a41c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a41c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8a41c-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a41c-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a41c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a41c-121">Library</span></span><br/> | <dl> <span data-ttu-id="8a41c-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8a41c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a41c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a41c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a41c-124">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="8a41c-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




