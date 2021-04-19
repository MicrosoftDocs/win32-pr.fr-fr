---
description: La méthode SetTargetRect définit le rectangle cible.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Méthode CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528710"
---
# <a name="cdrawimagesettargetrect-method"></a><span data-ttu-id="f5a39-103">Méthode CDrawImage. SetTargetRect</span><span class="sxs-lookup"><span data-stu-id="f5a39-103">CDrawImage.SetTargetRect method</span></span>

<span data-ttu-id="f5a39-104">La `SetTargetRect` méthode définit le rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="f5a39-104">The `SetTargetRect` method sets the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5a39-105">Syntax</span></span>


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="f5a39-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5a39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a39-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="f5a39-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a39-108">Pointeur vers une structure **Rect** qui définit le nouveau rectangle cible.</span><span class="sxs-lookup"><span data-stu-id="f5a39-108">Pointer to a **RECT** structure that defines the new target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a39-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5a39-109">Return value</span></span>

<span data-ttu-id="f5a39-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f5a39-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a39-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f5a39-111">Remarks</span></span>

<span data-ttu-id="f5a39-112">Le filtre propriétaire doit appeler cette méthode si le rectangle source change ; par exemple, en réponse à un appel de [**IBasicVideo :: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .</span><span class="sxs-lookup"><span data-stu-id="f5a39-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) call.</span></span>

<span data-ttu-id="f5a39-113">Avant d’appeler cette méthode, validez le rectangle fourni dans *pTargetRect*, par rapport à la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="f5a39-113">Before calling this method, validate the rectangle given in *pTargetRect*, relative to the video window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a39-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a39-114">Requirements</span></span>



| <span data-ttu-id="f5a39-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a39-115">Requirement</span></span> | <span data-ttu-id="f5a39-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a39-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a39-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5a39-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a39-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a39-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5a39-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5a39-119">Library</span></span><br/> | <dl> <span data-ttu-id="f5a39-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a39-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a39-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a39-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a39-122">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="f5a39-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




