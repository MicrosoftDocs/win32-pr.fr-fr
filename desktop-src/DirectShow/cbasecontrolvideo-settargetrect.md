---
description: La méthode SetTargetRect définit le rectangle cible actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle de destination change.
ms.assetid: 9e48989d-5995-4f9d-82b2-01229473c3e8
title: Méthode CBaseControlVideo. SetTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3868e7d8df93940829fb96c7152a55048a5cae82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535370"
---
# <a name="cbasecontrolvideosettargetrect-method"></a><span data-ttu-id="49393-104">Méthode CBaseControlVideo. SetTargetRect</span><span class="sxs-lookup"><span data-stu-id="49393-104">CBaseControlVideo.SetTargetRect method</span></span>

<span data-ttu-id="49393-105">La `SetTargetRect` méthode définit le rectangle cible actuel (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="49393-105">The `SetTargetRect` method sets the current target rectangle (pure virtual).</span></span> <span data-ttu-id="49393-106">Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle de destination change.</span><span class="sxs-lookup"><span data-stu-id="49393-106">This is an internal member function that gets called when the destination rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="49393-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49393-107">Syntax</span></span>


```C++
virtual HRESULT SetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="49393-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49393-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49393-109">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="49393-109">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="49393-110">Pointeur vers le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="49393-110">Pointer to the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49393-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49393-111">Return value</span></span>

<span data-ttu-id="49393-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49393-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49393-113">Notes</span><span class="sxs-lookup"><span data-stu-id="49393-113">Remarks</span></span>

<span data-ttu-id="49393-114">Les classes dérivées doivent remplacer cette valeur pour savoir quand le rectangle de destination change.</span><span class="sxs-lookup"><span data-stu-id="49393-114">Derived classes should override this to know when the destination rectangle changes.</span></span> <span data-ttu-id="49393-115">Elle est appelée à partir des fonctions membres suivantes.</span><span class="sxs-lookup"><span data-stu-id="49393-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="49393-116">**CBaseControlVideo::SetDestinationPosition**</span><span class="sxs-lookup"><span data-stu-id="49393-116">**CBaseControlVideo::SetDestinationPosition**</span></span>](cbasecontrolvideo-setdestinationposition.md)
-   [<span data-ttu-id="49393-117">**CBaseControlVideo ::p ut \_ DestinationLeft**</span><span class="sxs-lookup"><span data-stu-id="49393-117">**CBaseControlVideo::put\_DestinationLeft**</span></span>](cbasecontrolvideo-put-destinationleft.md)
-   [<span data-ttu-id="49393-118">**CBaseControlVideo ::p ut \_ DestinationWidth**</span><span class="sxs-lookup"><span data-stu-id="49393-118">**CBaseControlVideo::put\_DestinationWidth**</span></span>](cbasecontrolvideo-put-destinationwidth.md)
-   [<span data-ttu-id="49393-119">**CBaseControlVideo ::p ut \_ DestinationTop**</span><span class="sxs-lookup"><span data-stu-id="49393-119">**CBaseControlVideo::put\_DestinationTop**</span></span>](cbasecontrolvideo-put-destinationtop.md)
-   [<span data-ttu-id="49393-120">**CBaseControlVideo ::p ut \_ DestinationHeight**</span><span class="sxs-lookup"><span data-stu-id="49393-120">**CBaseControlVideo::put\_DestinationHeight**</span></span>](cbasecontrolvideo-put-destinationheight.md)

<span data-ttu-id="49393-121">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="49393-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetTargetRect(RECT *pTargetRect)
{
    m_pRenderer->m_DrawImage.SetTargetRect(pTargetRect);
    return NOERROR;
}
```



<span data-ttu-id="49393-122">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="49393-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="49393-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49393-123">Requirements</span></span>



| <span data-ttu-id="49393-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49393-124">Requirement</span></span> | <span data-ttu-id="49393-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="49393-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49393-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="49393-126">Header</span></span><br/>  | <dl> <span data-ttu-id="49393-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49393-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49393-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="49393-128">Library</span></span><br/> | <dl> <span data-ttu-id="49393-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="49393-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49393-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49393-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49393-131">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="49393-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




