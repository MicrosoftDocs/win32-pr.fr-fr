---
description: La méthode SetSourceRect définit le rectangle source.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Méthode CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528638"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="c6c3e-103">Méthode CDrawImage. SetSourceRect</span><span class="sxs-lookup"><span data-stu-id="c6c3e-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="c6c3e-104">La `SetSourceRect` méthode définit le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="c6c3e-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6c3e-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="c6c3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6c3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c3e-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="c6c3e-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c3e-108">Pointeur vers une structure **Rect** qui définit le nouveau rectangle source.</span><span class="sxs-lookup"><span data-stu-id="c6c3e-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c3e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6c3e-109">Return value</span></span>

<span data-ttu-id="c6c3e-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c6c3e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6c3e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6c3e-111">Remarks</span></span>

<span data-ttu-id="c6c3e-112">Le filtre propriétaire doit appeler cette méthode si le rectangle source change ; par exemple, en réponse à un appel de [**IBasicVideo :: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .</span><span class="sxs-lookup"><span data-stu-id="c6c3e-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="c6c3e-113">Validez le rectangle donné dans *pSourceRect* avant d’appeler cette méthode pour vous assurer qu’il ne s’étend pas au-delà de la taille de la vidéo native.</span><span class="sxs-lookup"><span data-stu-id="c6c3e-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c3e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6c3e-114">Requirements</span></span>



| <span data-ttu-id="c6c3e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6c3e-115">Requirement</span></span> | <span data-ttu-id="c6c3e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c3e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c3e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6c3e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c3e-118"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c3e-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6c3e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6c3e-119">Library</span></span><br/> | <dl> <span data-ttu-id="c6c3e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c3e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c3e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c3e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c3e-122">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="c6c3e-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




