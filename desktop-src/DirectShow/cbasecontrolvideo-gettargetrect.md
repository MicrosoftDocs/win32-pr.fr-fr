---
description: La méthode GetTargetRect récupère le rectangle de destination. Il s’agit d’une fonction membre d’assistance interne.
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: Méthode CBaseControlVideo. GetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525467"
---
# <a name="cbasecontrolvideogettargetrect-method"></a><span data-ttu-id="de18e-104">Méthode CBaseControlVideo. GetTargetRect</span><span class="sxs-lookup"><span data-stu-id="de18e-104">CBaseControlVideo.GetTargetRect method</span></span>

<span data-ttu-id="de18e-105">La `GetTargetRect` méthode récupère le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="de18e-105">The `GetTargetRect` method retrieves the destination rectangle.</span></span> <span data-ttu-id="de18e-106">Il s’agit d’une fonction membre d’assistance interne.</span><span class="sxs-lookup"><span data-stu-id="de18e-106">This is an internal helper member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="de18e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de18e-107">Syntax</span></span>


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="de18e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de18e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de18e-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="de18e-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="de18e-110">Pointeur vers le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="de18e-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de18e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de18e-111">Return value</span></span>

<span data-ttu-id="de18e-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de18e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de18e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="de18e-113">Remarks</span></span>

<span data-ttu-id="de18e-114">Cette fonction membre doit être substituée dans la classe dérivée pour retourner le rectangle cible détenu par le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="de18e-114">This member function must be overridden in the derived class to return the target rectangle held by the video renderer.</span></span> <span data-ttu-id="de18e-115">Elle est appelée à partir des fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="de18e-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="de18e-116">**CBaseControlVideo::GetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="de18e-116">**CBaseControlVideo::GetDestinationPosition**</span></span>](cbasecontrolvideo-getdestinationposition.md)
-   [<span data-ttu-id="de18e-117">**CBaseControlVideo ::p ut \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="de18e-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="de18e-118">**CBaseControlVideo :: obtient \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="de18e-118">**CBaseControlVideo::get\_DestinationLeft**</span></span>](cbasecontrolvideo-get-destinationleft.md)
-   [<span data-ttu-id="de18e-119">**CBaseControlVideo ::p ut \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="de18e-119">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="de18e-120">**CBaseControlVideo :: obtient \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="de18e-120">**CBaseControlVideo::get\_DestinationWidth**</span></span>](cbasecontrolvideo-get-destinationwidth.md)
-   [<span data-ttu-id="de18e-121">**CBaseControlVideo ::p ut \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="de18e-121">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="de18e-122">**CBaseControlVideo :: obtient \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="de18e-122">**CBaseControlVideo::get\_DestinationTop**</span></span>](cbasecontrolvideo-get-destinationtop.md)
-   [<span data-ttu-id="de18e-123">**CBaseControlVideo ::p ut \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="de18e-123">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)
-   [<span data-ttu-id="de18e-124">**CBaseControlVideo :: obtient \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="de18e-124">**CBaseControlVideo::get\_DestinationHeight**</span></span>](cbasecontrolvideo-get-destinationheight.md)

<span data-ttu-id="de18e-125">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="de18e-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="de18e-126">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="de18e-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="de18e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de18e-127">Requirements</span></span>



| <span data-ttu-id="de18e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de18e-128">Requirement</span></span> | <span data-ttu-id="de18e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="de18e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de18e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="de18e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="de18e-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de18e-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de18e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="de18e-132">Library</span></span><br/> | <dl> <span data-ttu-id="de18e-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de18e-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de18e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de18e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de18e-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="de18e-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




