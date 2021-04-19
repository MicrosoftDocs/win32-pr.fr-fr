---
description: La méthode IsDefaultSourceRect détermine si le convertisseur utilise le rectangle source par défaut (virtuel pur).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Méthode CBaseControlVideo. IsDefaultSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390ae779eaa7d640d23b40a7e6f6579e158bf6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534857"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a><span data-ttu-id="991a9-103">Méthode CBaseControlVideo. IsDefaultSourceRect</span><span class="sxs-lookup"><span data-stu-id="991a9-103">CBaseControlVideo.IsDefaultSourceRect method</span></span>

<span data-ttu-id="991a9-104">La `IsDefaultSourceRect` méthode détermine si le convertisseur utilise le rectangle source par défaut (virtuel pur).</span><span class="sxs-lookup"><span data-stu-id="991a9-104">The `IsDefaultSourceRect` method determines if the renderer is using the default source rectangle (pure virtual).</span></span>

## <a name="syntax"></a><span data-ttu-id="991a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="991a9-105">Syntax</span></span>


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a><span data-ttu-id="991a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="991a9-106">Parameters</span></span>

<span data-ttu-id="991a9-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="991a9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="991a9-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="991a9-108">Return value</span></span>

<span data-ttu-id="991a9-109">Retourne S \_ OK si le convertisseur utilise la source par défaut ; sinon, retourne s \_ false.</span><span class="sxs-lookup"><span data-stu-id="991a9-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="991a9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="991a9-110">Remarks</span></span>

<span data-ttu-id="991a9-111">Cette fonction membre doit être implémentée dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="991a9-111">This member function must be implemented in the derived class.</span></span> <span data-ttu-id="991a9-112">Elle est appelée par la fonction membre [**CBaseControlVideo :: IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) .</span><span class="sxs-lookup"><span data-stu-id="991a9-112">It is called by the [**CBaseControlVideo::IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) member function.</span></span>

<span data-ttu-id="991a9-113">L’exemple suivant illustre une implémentation de cette fonction dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="991a9-113">The following example demonstrates an implementation of this function in a derived class.</span></span>


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



<span data-ttu-id="991a9-114">Dans cet exemple, CVideoText est une classe dérivée de [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md), et le membre de \_ données m DrawImage, défini dans la classe dérivée, contient un objet [**CDrawImage**](cdrawimage.md) .</span><span class="sxs-lookup"><span data-stu-id="991a9-114">In this example, CVideoText is a class derived from [**CBaseControlVideo**](cbasecontrolvideo.md), m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md), and the m\_DrawImage data member, defined in the derived class, holds a [**CDrawImage**](cdrawimage.md) object.</span></span> <span data-ttu-id="991a9-115">Le \_ membre de données m mtIn, également défini dans la classe dérivée, contient un objet [**CMediaType**](cmediatype.md) avec le type de média de la broche d’entrée.</span><span class="sxs-lookup"><span data-stu-id="991a9-115">The m\_mtIn data member, also defined in the derived class, holds a [**CMediaType**](cmediatype.md) object with the media type of the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="991a9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="991a9-116">Requirements</span></span>



| <span data-ttu-id="991a9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="991a9-117">Requirement</span></span> | <span data-ttu-id="991a9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="991a9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991a9-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="991a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="991a9-120"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="991a9-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="991a9-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="991a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="991a9-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="991a9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991a9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="991a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991a9-124">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="991a9-124">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




