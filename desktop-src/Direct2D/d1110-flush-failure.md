---
title: Échec du vidage de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Échec d’un appel de vidage par une cible de rendu
keywords:
- Erreur de vidage D1110 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 721fb27e8cfd5e83f94b93079ee66e4a1c35992d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549924"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="f1ce8-104">D1110 : échec de vidage</span><span class="sxs-lookup"><span data-stu-id="f1ce8-104">D1110: Flush Failure</span></span>

<span data-ttu-id="f1ce8-105">Un appel de vidage par une cible de rendu a échoué \[  \] .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="f1ce8-106">Balises \[ *: étiquette1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="f1ce8-107">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="f1ce8-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="f1ce8-108"><span id="resource"></span><span id="RESOURCE"></span>*ressource*</span><span class="sxs-lookup"><span data-stu-id="f1ce8-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="f1ce8-109">Adresse de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="f1ce8-110"><span id="tag1"></span><span id="TAG1"></span>*: étiquette1*</span><span class="sxs-lookup"><span data-stu-id="f1ce8-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="f1ce8-111">Première valeur de la balise.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-111">The first tag value.</span></span> <span data-ttu-id="f1ce8-112">Pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="f1ce8-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="f1ce8-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="f1ce8-114">Deuxième valeur de balise.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-114">The second tag value.</span></span> <span data-ttu-id="f1ce8-115">Pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="f1ce8-116">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="f1ce8-116">Error Level</span></span> | <span data-ttu-id="f1ce8-117">Avertissement</span><span class="sxs-lookup"><span data-stu-id="f1ce8-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="f1ce8-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="f1ce8-118">Examples</span></span>

<span data-ttu-id="f1ce8-119">**Exemple 1 :** Le code suivant montre qu’un appel de dessin est dans un État non valide.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="f1ce8-120">Pour éviter le message d’avertissement, utilisez [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) pour définir l’anticrénelage du mode anticrénelage d2d1 \_ \_ \_ avant un appel [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="f1ce8-121">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="f1ce8-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="f1ce8-122">**Exemple 2 :** Le code suivant montre que le [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé après l’appel [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="f1ce8-123">Cet exemple génère le message de débogage suivant :</span><span class="sxs-lookup"><span data-stu-id="f1ce8-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="f1ce8-124">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="f1ce8-124">Possible Causes</span></span>

<span data-ttu-id="f1ce8-125">L’appel de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) peut échouer pour l’une des deux raisons suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="f1ce8-126">Elle peut échouer parce que la méthode a été appelée en dehors de l’appel [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , ou elle peut échouer en raison d’une erreur produite par l’une des opérations de la cible de rendu qui ont été traitées depuis le dernier appel de **vidage** ou l’appel **EndDraw** .</span><span class="sxs-lookup"><span data-stu-id="f1ce8-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="f1ce8-127">Pour résoudre le problème, l’application doit déterminer la cause de l’erreur et prendre les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="f1ce8-128">Correctifs</span><span class="sxs-lookup"><span data-stu-id="f1ce8-128">Fixes</span></span>

<span data-ttu-id="f1ce8-129">Il existe de nombreuses raisons pour lesquelles un appel de [**vidage**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) peut échouer.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="f1ce8-130">L’application doit déterminer la cause de l’erreur et prendre les mesures appropriées.</span><span class="sxs-lookup"><span data-stu-id="f1ce8-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 