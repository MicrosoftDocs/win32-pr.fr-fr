---
description: La méthode GetSourceRect récupère le rectangle source. Il s’agit d’une méthode interne.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Méthode CBaseControlVideo. GetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e57a5beda7b147e952ecbb26c96df5f7e372e6d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528089"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a><span data-ttu-id="f87cc-104">Méthode CBaseControlVideo. GetSourceRect</span><span class="sxs-lookup"><span data-stu-id="f87cc-104">CBaseControlVideo.GetSourceRect method</span></span>

<span data-ttu-id="f87cc-105">La `GetSourceRect` méthode récupère le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="f87cc-105">The `GetSourceRect` method retrieves the source rectangle.</span></span> <span data-ttu-id="f87cc-106">Il s’agit d’une méthode interne.</span><span class="sxs-lookup"><span data-stu-id="f87cc-106">This is an internal method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87cc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f87cc-107">Syntax</span></span>


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f87cc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f87cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87cc-109">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f87cc-109">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f87cc-110">Pointeur vers le rectangle source récupéré.</span><span class="sxs-lookup"><span data-stu-id="f87cc-110">Pointer to the retrieved source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87cc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f87cc-111">Return value</span></span>

<span data-ttu-id="f87cc-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f87cc-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f87cc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f87cc-113">Remarks</span></span>

<span data-ttu-id="f87cc-114">Cette fonction membre doit être substituée dans la classe dérivée pour retourner le rectangle source détenu par le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="f87cc-114">This member function must be overridden in the derived class to return the source rectangle held by the video renderer.</span></span> <span data-ttu-id="f87cc-115">Elle est appelée à partir des fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.</span><span class="sxs-lookup"><span data-stu-id="f87cc-115">It is called from the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="f87cc-116">**CBaseControlVideo::GetSourcePosition**</span><span class="sxs-lookup"><span data-stu-id="f87cc-116">**CBaseControlVideo::GetSourcePosition**</span></span>](cbasecontrolvideo-getsourceposition.md)
-   [<span data-ttu-id="f87cc-117">**CBaseControlVideo ::p ut \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f87cc-117">**CBaseControlVideo::put\_SourceLeft**</span></span>](cbasecontrolvideo-put-sourceleft.md)
-   [<span data-ttu-id="f87cc-118">**CBaseControlVideo :: obtient \_ SourceLeft**</span><span class="sxs-lookup"><span data-stu-id="f87cc-118">**CBaseControlVideo::get\_SourceLeft**</span></span>](cbasecontrolvideo-get-sourceleft.md)
-   [<span data-ttu-id="f87cc-119">**CBaseControlVideo ::p ut \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f87cc-119">**CBaseControlVideo::put\_SourceWidth**</span></span>](cbasecontrolvideo-put-sourcewidth.md)
-   [<span data-ttu-id="f87cc-120">**CBaseControlVideo :: obtient \_ SourceWidth**</span><span class="sxs-lookup"><span data-stu-id="f87cc-120">**CBaseControlVideo::get\_SourceWidth**</span></span>](cbasecontrolvideo-get-sourcewidth.md)
-   [<span data-ttu-id="f87cc-121">**CBaseControlVideo ::p ut \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="f87cc-121">**CBaseControlVideo::put\_SourceTop**</span></span>](cbasecontrolvideo-put-sourcetop.md)
-   [<span data-ttu-id="f87cc-122">**CBaseControlVideo :: obtient \_ sourceTop**</span><span class="sxs-lookup"><span data-stu-id="f87cc-122">**CBaseControlVideo::get\_SourceTop**</span></span>](cbasecontrolvideo-get-sourcetop.md)
-   [<span data-ttu-id="f87cc-123">**CBaseControlVideo ::p ut \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f87cc-123">**CBaseControlVideo::put\_SourceHeight**</span></span>](cbasecontrolvideo-put-sourceheight.md)
-   [<span data-ttu-id="f87cc-124">**CBaseControlVideo :: obtient \_ SourceHeight**</span><span class="sxs-lookup"><span data-stu-id="f87cc-124">**CBaseControlVideo::get\_SourceHeight**</span></span>](cbasecontrolvideo-get-sourceheight.md)

<span data-ttu-id="f87cc-125">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="f87cc-125">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



<span data-ttu-id="f87cc-126">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="f87cc-126">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87cc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f87cc-127">Requirements</span></span>



| <span data-ttu-id="f87cc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f87cc-128">Requirement</span></span> | <span data-ttu-id="f87cc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f87cc-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87cc-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f87cc-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f87cc-131"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f87cc-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f87cc-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f87cc-132">Library</span></span><br/> | <dl> <span data-ttu-id="f87cc-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f87cc-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87cc-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f87cc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87cc-135">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="f87cc-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




