---
description: La méthode SetDefaultTargetRect définit le rectangle vidéo cible par défaut (virtuel pur). Il s’agit d’une fonction membre interne qui est appelée lors de la réinitialisation du rectangle source.
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: Méthode CBaseControlVideo. SetDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54b31268935cb296543b3992bf67b7a2193c1a92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527311"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a><span data-ttu-id="e6803-104">Méthode CBaseControlVideo. SetDefaultTargetRect</span><span class="sxs-lookup"><span data-stu-id="e6803-104">CBaseControlVideo.SetDefaultTargetRect method</span></span>

<span data-ttu-id="e6803-105">La `SetDefaultTargetRect` méthode définit le rectangle vidéo cible par défaut (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="e6803-105">The `SetDefaultTargetRect` method sets the default target video rectangle (pure virtual).</span></span> <span data-ttu-id="e6803-106">Il s’agit d’une fonction membre interne qui est appelée lors de la réinitialisation du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="e6803-106">This is an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6803-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6803-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="e6803-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6803-108">Parameters</span></span>

<span data-ttu-id="e6803-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6803-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6803-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6803-110">Return value</span></span>

<span data-ttu-id="e6803-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6803-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6803-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e6803-112">Remarks</span></span>

<span data-ttu-id="e6803-113">Les classes dérivées doivent remplacer cette valeur pour réinitialiser le rectangle vidéo de destination.</span><span class="sxs-lookup"><span data-stu-id="e6803-113">Derived classes should override this to reset the destination video rectangle.</span></span> <span data-ttu-id="e6803-114">Elle est appelée à partir de la fonction membre [**CBaseControlVideo :: SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) .</span><span class="sxs-lookup"><span data-stu-id="e6803-114">It is called from the [**CBaseControlVideo::SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) member function.</span></span>

<span data-ttu-id="e6803-115">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e6803-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



<span data-ttu-id="e6803-116">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="e6803-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="e6803-117">Le \_ membre de données m mtIn, également défini dans la classe dérivée, contient un objet [**CMediaType**](cmediatype.md) avec le type de média de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e6803-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6803-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6803-118">Requirements</span></span>



| <span data-ttu-id="e6803-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6803-119">Requirement</span></span> | <span data-ttu-id="e6803-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6803-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6803-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6803-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e6803-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6803-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6803-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6803-123">Library</span></span><br/> | <dl> <span data-ttu-id="e6803-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6803-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6803-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6803-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6803-126">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="e6803-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




