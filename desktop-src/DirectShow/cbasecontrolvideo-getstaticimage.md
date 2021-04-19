---
description: Méthode virtuelle pure substituée par les classes dérivées.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Méthode CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520964"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="15fab-103">Méthode CBaseControlVideo. GetStaticImage</span><span class="sxs-lookup"><span data-stu-id="15fab-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="15fab-104">Méthode virtuelle pure substituée par les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="15fab-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15fab-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="15fab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15fab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fab-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="15fab-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="15fab-108">Pointeur vers la taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="15fab-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="15fab-109">*pDIBImage*</span><span class="sxs-lookup"><span data-stu-id="15fab-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="15fab-110">Pointeur vers la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="15fab-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fab-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15fab-111">Return value</span></span>

<span data-ttu-id="15fab-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15fab-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15fab-113">Notes</span><span class="sxs-lookup"><span data-stu-id="15fab-113">Remarks</span></span>

<span data-ttu-id="15fab-114">Par le biais de l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , une application peut demander à recevoir une copie de l’image actuelle dans une mémoire tampon (certains convertisseurs peuvent retourner E \_ NOTIMPL à cet objet s’ils ne le prennent pas en charge).</span><span class="sxs-lookup"><span data-stu-id="15fab-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="15fab-115">La classe dérivée détermine comment récupérer l’image.</span><span class="sxs-lookup"><span data-stu-id="15fab-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="15fab-116">Lorsque l’application appelle **CBaseControlVideo :: GetStaticImage**, elle appelle cette méthode virtuelle pure que la classe dérivée doit substituer pour l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="15fab-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="15fab-117">Cela est également appelé par la fonction membre [**CBaseControlVideo :: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .</span><span class="sxs-lookup"><span data-stu-id="15fab-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="15fab-118">La classe fournit une fonction membre d’assistance, [**CBaseControlVideo :: CopyImage**](cbasecontrolvideo-copyimage.md), qui peut recevoir un exemple qui contient une image, et la fonction membre copie la section pertinente de celle-ci (en fonction du rectangle source actuel) dans la mémoire tampon de sortie fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="15fab-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="15fab-119">L’exemple suivant illustre une implémentation de cette fonction membre dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="15fab-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="15fab-120">Dans cet exemple, m \_ pRenderer contient un objet d’une classe dérivée de [**CBaseVideoRenderer**](cbasevideorenderer.md).</span><span class="sxs-lookup"><span data-stu-id="15fab-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="15fab-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15fab-121">Requirements</span></span>



| <span data-ttu-id="15fab-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15fab-122">Requirement</span></span> | <span data-ttu-id="15fab-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="15fab-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fab-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="15fab-124">Header</span></span><br/>  | <dl> <span data-ttu-id="15fab-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15fab-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15fab-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15fab-126">Library</span></span><br/> | <dl> <span data-ttu-id="15fab-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15fab-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fab-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15fab-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fab-129">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="15fab-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




