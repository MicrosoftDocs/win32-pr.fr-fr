---
description: La méthode SetSourceRect définit le rectangle vidéo source actuel (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle source est modifié.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Méthode CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537863"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a><span data-ttu-id="e0034-104">Méthode CBaseControlVideo. SetSourceRect</span><span class="sxs-lookup"><span data-stu-id="e0034-104">CBaseControlVideo.SetSourceRect method</span></span>

<span data-ttu-id="e0034-105">La `SetSourceRect` méthode définit le rectangle vidéo source actuel (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="e0034-105">The `SetSourceRect` method sets the current source video rectangle (pure virtual).</span></span> <span data-ttu-id="e0034-106">Il s’agit d’une fonction membre interne qui est appelée lorsque le rectangle source est modifié.</span><span class="sxs-lookup"><span data-stu-id="e0034-106">This is an internal member function that gets called when the source rectangle changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0034-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0034-107">Syntax</span></span>


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e0034-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0034-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0034-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="e0034-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="e0034-110">Pointeur vers le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="e0034-110">Pointer to the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0034-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0034-111">Return value</span></span>

<span data-ttu-id="e0034-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0034-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0034-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e0034-113">Remarks</span></span>

<span data-ttu-id="e0034-114">Les classes dérivées doivent remplacer cette fonction membre pour savoir quand le rectangle source change.</span><span class="sxs-lookup"><span data-stu-id="e0034-114">Derived classes should override this member function to know when the source rectangle changes.</span></span> <span data-ttu-id="e0034-115">Elle est appelée à partir des fonctions membres suivantes.</span><span class="sxs-lookup"><span data-stu-id="e0034-115">It is called from the following member functions.</span></span>

-   [<span data-ttu-id="e0034-116">**CBaseControlVideo::SetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="e0034-116">**CBaseControlVideo::SetSourcePosition**</span></span>](cbasecontrolvideo-setsourceposition.md)
-   [<span data-ttu-id="e0034-117">**CBaseControlVideo ::p ut \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="e0034-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="e0034-118">**CBaseControlVideo ::p ut \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="e0034-118">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="e0034-119">**CBaseControlVideo ::p ut \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="e0034-119">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="e0034-120">**CBaseControlVideo ::p ut \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="e0034-120">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)

<span data-ttu-id="e0034-121">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0034-121">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="e0034-122">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="e0034-122">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0034-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0034-123">Requirements</span></span>



| <span data-ttu-id="e0034-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0034-124">Requirement</span></span> | <span data-ttu-id="e0034-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0034-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0034-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0034-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e0034-127"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0034-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0034-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e0034-128">Library</span></span><br/> | <dl> <span data-ttu-id="e0034-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e0034-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0034-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0034-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0034-131">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="e0034-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




