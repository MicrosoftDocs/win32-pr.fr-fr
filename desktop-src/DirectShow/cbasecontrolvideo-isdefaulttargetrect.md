---
description: La méthode IsDefaultTargetRect détermine si le convertisseur utilise le rectangle cible par défaut (virtuel pur).
ms.assetid: 60c09515-7a34-421c-b3e8-ce746a935583
title: Méthode CBaseControlVideo. IsDefaultTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e267cc65345d18800beccbc80ac7952c89d781d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533499"
---
# <a name="cbasecontrolvideoisdefaulttargetrect-method"></a><span data-ttu-id="4ec91-103">Méthode CBaseControlVideo. IsDefaultTargetRect</span><span class="sxs-lookup"><span data-stu-id="4ec91-103">CBaseControlVideo.IsDefaultTargetRect method</span></span>

<span data-ttu-id="4ec91-104">La `IsDefaultTargetRect` méthode détermine si le convertisseur utilise le rectangle cible par défaut (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="4ec91-104">The `IsDefaultTargetRect` method determines if the renderer is using the default target rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ec91-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultTargetRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="4ec91-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ec91-106">Parameters</span></span>

<span data-ttu-id="4ec91-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4ec91-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ec91-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ec91-108">Return value</span></span>

<span data-ttu-id="4ec91-109">Retourne S \_ OK si le convertisseur utilise la cible par défaut ; sinon, retourne s \_ false.</span><span class="sxs-lookup"><span data-stu-id="4ec91-109">Returns S\_OK if the renderer is using the default target; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ec91-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4ec91-110">Remarks</span></span>

<span data-ttu-id="4ec91-111">Cette fonction membre doit être implémentée dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="4ec91-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="4ec91-112">Elle est appelée par la fonction membre [**CBaseControlVideo :: IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec91-112">It is called by the [**CBaseControlVideo::IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md) member function.</span></span>

<span data-ttu-id="4ec91-113">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="4ec91-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default target; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultTargetRect()
{
    RECT TargetRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetTargetRect(&TargetRect);

    // Check the destination that matches the initial client area.

    if (TargetRect.left != 0 || TargetRect.top != 0 ||
            TargetRect.right != m_Size.cx ||
                TargetRect.bottom != m_Size.cy) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="4ec91-114">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec91-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="4ec91-115">Le \_ membre de données m mtIn, également défini dans la classe dérivée, contient un objet [**CMediaType**](cmediatype.md) avec le type de média de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="4ec91-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec91-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ec91-116">Requirements</span></span>



| <span data-ttu-id="4ec91-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ec91-117">Requirement</span></span> | <span data-ttu-id="4ec91-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ec91-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec91-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ec91-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4ec91-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ec91-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4ec91-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4ec91-121">Library</span></span><br/> | <dl> <span data-ttu-id="4ec91-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4ec91-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ec91-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ec91-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec91-124">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="4ec91-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




