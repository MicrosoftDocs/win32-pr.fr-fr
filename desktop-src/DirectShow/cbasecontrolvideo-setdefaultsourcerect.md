---
description: La méthode SetDefaultSourceRect définit le rectangle de la vidéo source par défaut (virtuel pur). Dans une fonction membre interne qui est appelée lors de la réinitialisation du rectangle source.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Méthode CBaseControlVideo. SetDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fe2001a42ca75fff4f3172c8ce05da18881d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525520"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a><span data-ttu-id="31589-104">Méthode CBaseControlVideo. SetDefaultSourceRect</span><span class="sxs-lookup"><span data-stu-id="31589-104">CBaseControlVideo.SetDefaultSourceRect method</span></span>

<span data-ttu-id="31589-105">La `SetDefaultSourceRect` méthode définit le rectangle de la vidéo source par défaut (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="31589-105">The `SetDefaultSourceRect` method sets the default source video rectangle (pure virtual).</span></span> <span data-ttu-id="31589-106">Dans une fonction membre interne qui est appelée lors de la réinitialisation du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="31589-106">This in an internal member function that gets called when the source rectangle is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="31589-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31589-107">Syntax</span></span>


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="31589-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31589-108">Parameters</span></span>

<span data-ttu-id="31589-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="31589-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31589-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31589-110">Return value</span></span>

<span data-ttu-id="31589-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31589-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31589-112">Notes</span><span class="sxs-lookup"><span data-stu-id="31589-112">Remarks</span></span>

<span data-ttu-id="31589-113">Les classes dérivées doivent remplacer cette valeur pour réinitialiser le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="31589-113">Derived classes should override this to reset the source rectangle.</span></span> <span data-ttu-id="31589-114">Elle est appelée à partir de [**CBaseControlVideo :: SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span><span class="sxs-lookup"><span data-stu-id="31589-114">It is called from [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).</span></span>

<span data-ttu-id="31589-115">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="31589-115">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



<span data-ttu-id="31589-116">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="31589-116">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="31589-117">Le \_ membre de données m mtIn, également défini dans la classe dérivée, contient un objet [**CMediaType**](cmediatype.md) avec le type de média de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="31589-117">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="31589-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31589-118">Requirements</span></span>



| <span data-ttu-id="31589-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31589-119">Requirement</span></span> | <span data-ttu-id="31589-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="31589-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31589-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="31589-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31589-122"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31589-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31589-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="31589-123">Library</span></span><br/> | <dl> <span data-ttu-id="31589-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="31589-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31589-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31589-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31589-126">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="31589-126">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




